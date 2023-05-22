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

```bash
$ export KUBECONFIG=/home/tamal/Downloads/tamal-us-west-kubeconfig.yaml

$ k get nodes -o wide
NAME                            STATUS   ROLES    AGE   VERSION   INTERNAL-IP       EXTERNAL-IP    OS-IMAGE                         KERNEL-VERSION          CONTAINER-RUNTIME
lke109602-163536-646b6c5c12e0   Ready    <none>   65m   v1.26.3   192.168.140.182   23.239.3.112   Debian GNU/Linux 11 (bullseye)   5.10.0-21-cloud-amd64   containerd://1.6.19
lke109602-163536-646b6c5c35c6   Ready    <none>   65m   v1.26.3   192.168.203.61    45.56.94.53    Debian GNU/Linux 11 (bullseye)   5.10.0-21-cloud-amd64   containerd://1.6.19
lke109602-163536-646b6c5c59b8   Ready    <none>   65m   v1.26.3   192.168.203.22    45.79.94.169   Debian GNU/Linux 11 (bullseye)   5.10.0-21-cloud-amd64   containerd://1.6.19
```

```bash
$ ssh root@45.79.94.169

# hostname -I
45.79.94.169 192.168.203.22 172.17.0.1 172.31.2.1 10.2.2.1 240.79.94.169 2600:3c01::f03c:93ff:feba:610e

# route -n
Kernel IP routing table
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
0.0.0.0         45.79.94.1      0.0.0.0         UG    0      0        0 eth0
10.2.0.0        192.168.140.182 255.255.255.0   UG    0      0        0 tunl0
10.2.1.0        192.168.203.61  255.255.255.0   UG    0      0        0 tunl0
10.2.2.0        0.0.0.0         255.255.255.0   U     0      0        0 *
10.2.2.7        0.0.0.0         255.255.255.255 UH    0      0        0 cali003dc3355f6
10.2.2.9        0.0.0.0         255.255.255.255 UH    0      0        0 calife180b4eb6f
10.2.2.10       0.0.0.0         255.255.255.255 UH    0      0        0 cali31f905d7fbc
45.79.94.0      0.0.0.0         255.255.255.0   U     0      0        0 eth0
172.17.0.0      0.0.0.0         255.255.0.0     U     0      0        0 docker0
172.31.255.1    0.0.0.0         255.255.255.255 UH    0      0        0 wg0
192.168.128.0   0.0.0.0         255.255.128.0   U     0      0        0 eth0
240.0.0.0       0.0.0.0         255.0.0.0       U     0      0        0 vx-submariner
242.0.0.0       240.239.3.112   255.255.0.0     UG    0      0        0 vx-submariner
```

```bash
$ ssh root@23.239.3.112

# hostname -I
23.239.3.112 192.168.140.182 172.17.0.1 172.31.0.1 10.2.0.1 240.239.3.112 2600:3c01::f03c:93ff:feba:61eb

# route -n
Kernel IP routing table
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
0.0.0.0         23.239.3.1      0.0.0.0         UG    0      0        0 eth0
10.2.0.0        0.0.0.0         255.255.255.0   U     0      0        0 *
10.2.0.2        0.0.0.0         255.255.255.255 UH    0      0        0 cali164b735c616
10.2.0.3        0.0.0.0         255.255.255.255 UH    0      0        0 cali7cb00f26386
10.2.0.4        0.0.0.0         255.255.255.255 UH    0      0        0 cali7dccccae91d
10.2.0.5        0.0.0.0         255.255.255.255 UH    0      0        0 cali4f9fb445c63
10.2.0.8        0.0.0.0         255.255.255.255 UH    0      0        0 calif879178337c
10.2.0.9        0.0.0.0         255.255.255.255 UH    0      0        0 cali315192acb59
10.2.1.0        192.168.203.61  255.255.255.0   UG    0      0        0 tunl0
10.2.2.0        192.168.203.22  255.255.255.0   UG    0      0        0 tunl0
23.239.3.0      0.0.0.0         255.255.255.0   U     0      0        0 eth0
172.17.0.0      0.0.0.0         255.255.0.0     U     0      0        0 docker0
172.31.255.1    0.0.0.0         255.255.255.255 UH    0      0        0 wg0
192.168.128.0   0.0.0.0         255.255.128.0   U     0      0        0 eth0
240.0.0.0       0.0.0.0         255.0.0.0       U     0      0        0 vx-submariner
242.0.0.0       -               255.255.0.0     !     0      -        0 -
```

```bash
$ kubectl run -n nginx-test tmp-shell --rm -i --tty --image quay.io/submariner/nettest -- /bin/bash


bash-5.0# dig nginx.nginx-test.svc.clusterset.local

; <<>> DiG 9.16.6 <<>> nginx.nginx-test.svc.clusterset.local
;; global options: +cmd
;; Got answer:
;; WARNING: .local is reserved for Multicast DNS
;; You are currently testing what happens when an mDNS query is leaked to DNS
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 46184
;; flags: qr aa rd; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1
;; WARNING: recursion requested but not available

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
; COOKIE: 12e8beb8cc978101 (echoed)
;; QUESTION SECTION:
;nginx.nginx-test.svc.clusterset.local. IN A

;; ANSWER SECTION:
nginx.nginx-test.svc.clusterset.local. 5 IN A	242.0.255.253

;; Query time: 4 msec
;; SERVER: 10.128.0.10#53(10.128.0.10)
;; WHEN: Mon May 22 14:23:53 UTC 2023
;; MSG SIZE  rcvd: 131


bash-5.0# traceroute 242.0.255.253
traceroute to 242.0.255.253 (242.0.255.253), 30 hops max, 46 byte packets
 1  45-79-94-169.ip.linodeusercontent.com (45.79.94.169)  0.005 ms  0.007 ms  0.002 ms
 2  10.2.0.1 (10.2.0.1)  0.415 ms  0.366 ms  0.245 ms
 3  *  *  *
 4  *  *  *
 5  *  *  *
 6  *  *  *
 7  *  *  *
 8  *  *^C

```
