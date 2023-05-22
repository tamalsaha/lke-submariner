# lke-submariner

## Test

- https://submariner.io/operations/usage/#2-export-services-across-clusters

### On us-east cluster

```bash
$ export KUBECONFIG=/home/tamal/Downloads/tamal-us-east-kubeconfig.yaml

$ kubectl create namespace nginx-test
namespace/nginx-test created
$ kubectl -n nginx-test create deployment nginx --image=nginxinc/nginx-unprivileged:stable-alpine
deployment.apps/nginx created

$ nano nginx-svc.yaml

$ kubectl -n nginx-test apply -f nginx-svc.yaml
service/nginx created
$ kubectl -n nginx-test get service nginx
NAME    TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
nginx   ClusterIP   10.128.213.36   <none>        8080/TCP   34s

$ kubectl -n nginx-test get pods -l app=nginx -o wide
NAME                     READY   STATUS    RESTARTS   AGE   IP         NODE                            NOMINATED NODE   READINESS GATES
nginx-5986b57d7c-xtqjf   1/1     Running   0          90s   10.2.2.9   lke109600-163534-646b6c274e5a   <none>           <none>

$ subctl export service --namespace nginx-test nginx
 ✓ Service exported successfully

$ kubectl get giip -A 
NAMESPACE    NAME    IP
nginx-test   nginx   242.0.255.253
```

### On us-west Cluster

```bash
$ export KUBECONFIG=/home/tamal/Downloads/tamal-us-west-kubeconfig.yaml

$ kubectl get -n submariner-operator serviceimport
NAME                               TYPE           IP                  AGE
nginx-nginx-test-cluster-us-east   ClusterSetIP   ["242.0.255.253"]   4m28s

$ kubectl run -n nginx-test tmp-shell --rm -i --tty --image quay.io/submariner/nettest -- /bin/bash
If you don't see a command prompt, try pressing enter.
bash-5.0# 
bash-5.0# dig nginx.nginx-test.svc.clusterset.local

; <<>> DiG 9.16.6 <<>> nginx.nginx-test.svc.clusterset.local
;; global options: +cmd
;; Got answer:
;; WARNING: .local is reserved for Multicast DNS
;; You are currently testing what happens when an mDNS query is leaked to DNS
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 36071
;; flags: qr aa rd; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1
;; WARNING: recursion requested but not available

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
; COOKIE: c0da46586ef0a936 (echoed)
;; QUESTION SECTION:
;nginx.nginx-test.svc.clusterset.local. IN A

;; ANSWER SECTION:
nginx.nginx-test.svc.clusterset.local. 5 IN A	242.0.255.253

;; Query time: 0 msec
;; SERVER: 10.128.0.10#53(10.128.0.10)
;; WHEN: Mon May 22 14:08:18 UTC 2023
;; MSG SIZE  rcvd: 131

bash-5.0# curl nginx.nginx-test.svc.clusterset.local:8080
curl: (28) Failed to connect to nginx.nginx-test.svc.clusterset.local port 8080: Operation timed out

```
