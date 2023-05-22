```
subctl join --kubeconfig /home/tamal/Downloads/tamal-us-east-kubeconfig.yaml broker-info.subm \
  --clusterid cluster-us-east \
  --globalnet \
  --clustercidr 10.2.0.0/16
  
subctl join --kubeconfig /home/tamal/Downloads/tamal-us-west-kubeconfig.yaml broker-info.subm \
  --clusterid cluster-us-west \
  --globalnet \
  --clustercidr 10.2.0.0/16
```

```
$ subctl verify \
   --context lke109600-ctx \
   --tocontext lke109602-ctx \
   --only service-discovery,connectivity --verbose

Performing the following verifications: service-discovery, connectivity
Running Suite: Submariner E2E suite
===================================
Random Seed: 1684778113
Will run 40 of 44 specs

STEP: Creating kubernetes clients
STEP: Setting new cluster ID "cluster-us-east", previous cluster ID was "lke109600"
STEP: Setting new cluster ID "cluster-us-west", previous cluster ID was "lke109602"
STEP: Creating lighthouse clients
STEP: Creating submariner clients
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote pod when the pod is not on a gateway and the remote pod is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-shx2b" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-shx2b" in cluster "cluster-us-west"
May 22 10:55:17.280: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-shx2b" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-shx2b" on cluster "cluster-us-west"

S [SKIPPING] [0.287 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:59
    when the pod is not on a gateway and the remote pod is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:67
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:17.280: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote pod when the pod is not on a gateway and the remote pod is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-v2mwx" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-v2mwx" in cluster "cluster-us-west"
May 22 10:55:17.565: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-v2mwx" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-v2mwx" on cluster "cluster-us-west"

S [SKIPPING] [0.288 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:59
    when the pod is not on a gateway and the remote pod is on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:71
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:17.565: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote pod when the pod is on a gateway and the remote pod is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-z5xkb" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-z5xkb" in cluster "cluster-us-west"
May 22 10:55:17.853: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-z5xkb" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-z5xkb" on cluster "cluster-us-west"

S [SKIPPING] [0.288 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:59
    when the pod is on a gateway and the remote pod is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:75
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:17.853: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote pod when the pod is on a gateway and the remote pod is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-bxvdj" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-bxvdj" in cluster "cluster-us-west"
May 22 10:55:18.140: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-bxvdj" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-bxvdj" on cluster "cluster-us-west"

S [SKIPPING] [0.289 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:59
    when the pod is on a gateway and the remote pod is on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:79
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:18.140: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote service when the pod is not on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-r785h" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-r785h" in cluster "cluster-us-west"
May 22 10:55:18.430: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-r785h" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-r785h" on cluster "cluster-us-west"

S [SKIPPING] [0.287 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:84
    when the pod is not on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:92
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:18.430: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote service when the pod is not on a gateway and the remote service is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-64phg" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-64phg" in cluster "cluster-us-west"
May 22 10:55:18.716: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-64phg" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-64phg" on cluster "cluster-us-west"

S [SKIPPING] [0.288 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:84
    when the pod is not on a gateway and the remote service is on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:96
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:18.716: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote service when the pod is on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-56p8x" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-56p8x" in cluster "cluster-us-west"
May 22 10:55:19.005: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-56p8x" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-56p8x" on cluster "cluster-us-west"

S [SKIPPING] [0.291 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:84
    when the pod is on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:100
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:19.005: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote service when the pod is on a gateway and the remote service is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-mg8tt" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-mg8tt" in cluster "cluster-us-west"
May 22 10:55:19.292: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-mg8tt" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-mg8tt" on cluster "cluster-us-west"

S [SKIPPING] [0.284 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:84
    when the pod is on a gateway and the remote service is on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:104
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:19.292: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod with HostNetworking connects via TCP to a remote pod when the pod is not on a gateway and the remote pod is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-dlmmt" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-dlmmt" in cluster "cluster-us-west"
May 22 10:55:19.580: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-dlmmt" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-dlmmt" on cluster "cluster-us-west"

S [SKIPPING] [0.291 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod with HostNetworking connects via TCP to a remote pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:109
    when the pod is not on a gateway and the remote pod is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:117
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:19.580: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod with HostNetworking connects via TCP to a remote pod when the pod is on a gateway and the remote pod is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-rgf8g" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-rgf8g" in cluster "cluster-us-west"
May 22 10:55:19.868: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-rgf8g" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-rgf8g" on cluster "cluster-us-west"

S [SKIPPING] [0.284 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod with HostNetworking connects via TCP to a remote pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:109
    when the pod is on a gateway and the remote pod is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:121
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:19.868: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Basic TCP connectivity tests across clusters without discovery when a pod connects via TCP to a remote pod in reverse direction when the pod is not on a gateway and the remote pod is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36
STEP: Creating namespace objects with basename "dataplane-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-conn-nd-tpql2" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-conn-nd-tpql2" in cluster "cluster-us-west"
May 22 10:55:20.156: INFO: Globalnet enabled, skipping the test...
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-tpql2" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-conn-nd-tpql2" on cluster "cluster-us-west"

S [SKIPPING] [0.292 seconds]
[dataplane] Basic TCP connectivity tests across clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:28
  when a pod connects via TCP to a remote pod in reverse direction
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:126
    when the pod is not on a gateway and the remote pod is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:134
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_pod_connectivity.go:36

      May 22 10:55:20.156: Globalnet enabled, skipping the test...

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/logging.go:60
------------------------------
[dataplane] Gateway status reporting when a gateway node is configured 
  should correctly report its status and connection information
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/gateway_status.go:38
STEP: Creating namespace objects with basename "dataplane-gateway-status"
STEP: Generated namespace "e2e-tests-dataplane-gateway-status-xn5lw" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gateway-status-xn5lw" in cluster "cluster-us-west"
STEP: Ensuring that only one gateway reports as active on "cluster-us-east"
STEP: Ensuring that gateway "lke109600-163534-646b6c270f06" reports connection information for cluster "cluster-us-west"
STEP: Deleting namespace "e2e-tests-dataplane-gateway-status-xn5lw" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gateway-status-xn5lw" on cluster "cluster-us-west"
•
------------------------------
[discovery] Test Stateful Sets Discovery Across Clusters when a pod tries to resolve a podname from stateful set in a remote cluster 
  should resolve the pod IP from the remote cluster
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/statefulsets.go:37
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-4xv4v" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-4xv4v" in cluster "cluster-us-west"
STEP: Creating an Nginx Stateful Set on "cluster-us-west"
STEP: Creating a Nginx Headless Service on "cluster-us-west"
STEP: Creating serviceExport nginx-ss.e2e-tests-discovery-4xv4v on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-ss.e2e-tests-discovery-4xv4v on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-ss" in ns "e2e-tests-discovery-4xv4v" on "cluster-us-west"
STEP: Executing "dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-4xv4v.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-ss" "are" discoverable
May 22 10:55:36.525: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-4xv4v.svc.clusterset.local] Namespace:e2e-tests-discovery-4xv4v PodName:netshoot5n2lh-6898dd765f-kcx49 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253"
STEP: Deleting serviceExport nginx-ss.e2e-tests-discovery-4xv4v on "cluster-us-west"
STEP: Retrieving EndpointSlices for "nginx-ss" in ns "e2e-tests-discovery-4xv4v" on "cluster-us-west"
STEP: Executing "dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-4xv4v.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-ss" "are not" discoverable
May 22 10:55:42.778: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-4xv4v.svc.clusterset.local] Namespace:e2e-tests-discovery-4xv4v PodName:netshoot5n2lh-6898dd765f-kcx49 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Deleting namespace "e2e-tests-discovery-4xv4v" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-4xv4v" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-4xv4v" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-4xv4v" on "cluster-us-east"
•
------------------------------
[discovery] Test Stateful Sets Discovery Across Clusters when a pod tries to resolve a podname from stateful set in a local cluster 
  should resolve the pod IP from the local cluster
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/statefulsets.go:43
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-fp7pm" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-fp7pm" in cluster "cluster-us-west"
STEP: Creating an Nginx Stateful Set on "cluster-us-west"
STEP: Creating a Nginx Headless Service on "cluster-us-west"
STEP: Creating an Nginx Stateful Set on "cluster-us-east"
STEP: Creating a Nginx Headless Service on "cluster-us-east"
STEP: Creating serviceExport nginx-ss.e2e-tests-discovery-fp7pm on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-ss.e2e-tests-discovery-fp7pm on "cluster-us-west"
STEP: Creating serviceExport nginx-ss.e2e-tests-discovery-fp7pm on "cluster-us-east"
STEP: Retrieving ServiceExport nginx-ss.e2e-tests-discovery-fp7pm on "cluster-us-east"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-ss" in ns "e2e-tests-discovery-fp7pm" on "cluster-us-west"
STEP: Executing "dig +short web-0.cluster-us-east.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local" to verify IPs [10.2.1.15] for service "nginx-ss" "are" discoverable
May 22 10:56:10.268: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-east.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local] Namespace:e2e-tests-discovery-fp7pm PodName:netshoot56jmw-6898dd765f-wr9bn ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "10.2.1.15"
STEP: Executing "dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-ss" "are" discoverable
May 22 10:56:10.899: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local] Namespace:e2e-tests-discovery-fp7pm PodName:netshoot56jmw-6898dd765f-wr9bn ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253"
STEP: Deleting serviceExport nginx-ss.e2e-tests-discovery-fp7pm on "cluster-us-west"
STEP: Executing "dig +short web-0.cluster-us-east.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local" to verify IPs [10.2.1.15] for service "nginx-ss" "are" discoverable
May 22 10:56:16.992: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-east.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local] Namespace:e2e-tests-discovery-fp7pm PodName:netshoot56jmw-6898dd765f-wr9bn ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "10.2.1.15"
STEP: Executing "dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-ss" "are not" discoverable
May 22 10:56:17.614: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-fp7pm.svc.clusterset.local] Namespace:e2e-tests-discovery-fp7pm PodName:netshoot56jmw-6898dd765f-wr9bn ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Deleting serviceExport nginx-ss.e2e-tests-discovery-fp7pm on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-ss" in ns "e2e-tests-discovery-fp7pm" on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-discovery-fp7pm" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-fp7pm" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-fp7pm" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-fp7pm" on "cluster-us-east"
•
------------------------------
[discovery] Test Stateful Sets Discovery Across Clusters when the number of active pods backing a stateful set changes 
  should only resolve the IPs from the active pods
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/statefulsets.go:49
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-5lvs9" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-5lvs9" in cluster "cluster-us-west"
STEP: Creating an Nginx Stateful Set on "cluster-us-west"
STEP: Setting Nginx statefulset replicas to 3
STEP: Creating a Nginx Headless Service on "cluster-us-west"
STEP: Creating serviceExport nginx-ss.e2e-tests-discovery-5lvs9 on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-ss.e2e-tests-discovery-5lvs9 on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-ss" in ns "e2e-tests-discovery-5lvs9" on "cluster-us-west"
STEP: Executing "dig +short web-2.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local" to verify IPs [242.1.255.251] for service "nginx-ss" "are" discoverable
May 22 10:56:34.652: INFO: ExecWithOptions &{Command:[dig +short web-2.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.251"
STEP: Executing "dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-ss" "are" discoverable
May 22 10:56:35.324: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253"
STEP: Executing "dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local" to verify IPs [242.1.255.252] for service "nginx-ss" "are" discoverable
May 22 10:56:35.948: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.252"
STEP: Setting Nginx statefulset replicas to 1
STEP: Executing "dig +short web-2.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local" to verify IPs [242.1.255.251] for service "nginx-ss" "are not" discoverable
May 22 10:56:36.621: INFO: ExecWithOptions &{Command:[dig +short web-2.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Executing "dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-ss" "are" discoverable
May 22 10:56:37.244: INFO: ExecWithOptions &{Command:[dig +short web-0.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253"
STEP: Executing "dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local" to verify IPs [242.1.255.252] for service "nginx-ss" "are not" discoverable
May 22 10:56:37.881: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "242.1.255.252"
May 22 10:56:43.544: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "242.1.255.252"
May 22 10:56:48.543: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "242.1.255.252"
May 22 10:56:53.564: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "242.1.255.252"
May 22 10:56:58.556: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "242.1.255.252"
May 22 10:57:03.552: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "242.1.255.252"
May 22 10:57:08.544: INFO: ExecWithOptions &{Command:[dig +short web-1.cluster-us-west.nginx-ss.e2e-tests-discovery-5lvs9.svc.clusterset.local] Namespace:e2e-tests-discovery-5lvs9 PodName:netshootbhwbh-6898dd765f-tqhdm ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Deleting serviceExport nginx-ss.e2e-tests-discovery-5lvs9 on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-discovery-5lvs9" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-5lvs9" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-5lvs9" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-5lvs9" on "cluster-us-east"
•SS
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-dhcr6" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-dhcr6" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 10:57:25.484: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says 1d955743-7e7b-41fd-851b-81396c13cadf; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-dhcr6 PodName:custom25jf9 ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c274e5a"
STEP: Waiting for the listener pod "tcp-check-listenerfgbfz" on node "lke109602-163536-646b6c5c35c6" to exit, returning what listener sent
May 22 11:00:26.257: INFO: Pod "tcp-check-listenerfgbfz" on node "lke109602-163536-646b6c5c35c6" output:
listening on 0.0.0.0:1234 ...
nc: timeout

STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-dhcr6" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-dhcr6" on cluster "cluster-us-west"

• Failure [191.908 seconds]
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:28
  when a pod connects via TCP to the globalIP of a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:60
    when the pod is not on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:69
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37

      Expected
          <int32>: 1
      to equal
          <int32>: 0

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote service when the pod is on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-xm2jr" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-xm2jr" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:00:42.814: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says 7a6500fb-5680-4802-935d-97e558799fdd; done | for i in $(seq 2); do if nc -v 242.1.255.252 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-xm2jr PodName:customtsc2k ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c270f06"
STEP: Waiting for the listener pod "tcp-check-listenerlnqch" on node "lke109602-163536-646b6c5c35c6" to exit, returning what listener sent
May 22 11:00:48.770: INFO: Pod "tcp-check-listenerlnqch" on node "lke109602-163536-646b6c5c35c6" output:
listening on 0.0.0.0:1234 ...
connect to 10.2.1.21:1234 from 242.0.0.3:43169 (242.0.0.3:43169)
[dataplane] connector says 7a6500fb-5680-4802-935d-97e558799fdd

STEP: Verifying that the listener got the connector's data and the connector got the listener's data
STEP: Verifying the output of the listener pod contains a cluster-scoped global IP [242.0.0.1 242.0.0.2 242.0.0.3 242.0.0.4 242.0.0.5 242.0.0.6 242.0.0.7 242.0.0.8] of the connector Pod
STEP: Deleting service "test-svc-tcp-check-listener" on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-xm2jr" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-xm2jr" on cluster "cluster-us-west"
•
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote service when the pod is on a gateway and the remote service is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-k4slc" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-k4slc" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:01:05.567: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says ebd894bc-635c-4a31-8ac9-87b0a5f9bdd9; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-k4slc PodName:customtlndc ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c270f06"
STEP: Waiting for the listener pod "tcp-check-listenerhdvvg" on node "lke109602-163536-646b6c5c12e0" to exit, returning what listener sent
May 22 11:01:11.421: INFO: Pod "tcp-check-listenerhdvvg" on node "lke109602-163536-646b6c5c12e0" output:
listening on 0.0.0.0:1234 ...
connect to 10.2.0.13:1234 from 242.0.0.3:33531 (242.0.0.3:33531)
[dataplane] connector says ebd894bc-635c-4a31-8ac9-87b0a5f9bdd9

STEP: Verifying that the listener got the connector's data and the connector got the listener's data
STEP: Verifying the output of the listener pod contains a cluster-scoped global IP [242.0.0.1 242.0.0.2 242.0.0.3 242.0.0.4 242.0.0.5 242.0.0.6 242.0.0.7 242.0.0.8] of the connector Pod
STEP: Deleting service "test-svc-tcp-check-listener" on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-k4slc" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-k4slc" on cluster "cluster-us-west"
•
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod matching an egress IP namespace selector connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-xl7r7" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-xl7r7" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:01:33.022: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says 7403e64c-73bd-4411-acf6-483c686d04d6; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-xl7r7 PodName:customnxlgn ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c274e5a"
STEP: Waiting for the listener pod "tcp-check-listener85gbr" on node "lke109602-163536-646b6c5c35c6" to exit, returning what listener sent
May 22 11:04:33.752: INFO: Pod "tcp-check-listener85gbr" on node "lke109602-163536-646b6c5c35c6" output:
listening on 0.0.0.0:1234 ...
nc: timeout

STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-xl7r7" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-xl7r7" on cluster "cluster-us-west"

• Failure [202.254 seconds]
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:28
  when a pod matching an egress IP namespace selector connects via TCP to the globalIP of a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:82
    when the pod is not on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:91
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37

      Expected
          <int32>: 1
      to equal
          <int32>: 0

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod matching an egress IP namespace selector connects via TCP to the globalIP of a remote service when the pod is on a gateway and the remote service is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-h6l6v" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-h6l6v" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:04:55.695: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says 7fec4a1e-43ab-433c-baba-20fb7bf1b0bb; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-h6l6v PodName:custom5q9fg ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c270f06"
STEP: Waiting for the listener pod "tcp-check-listener9qwl7" on node "lke109602-163536-646b6c5c12e0" to exit, returning what listener sent
May 22 11:05:01.581: INFO: Pod "tcp-check-listener9qwl7" on node "lke109602-163536-646b6c5c12e0" output:
listening on 0.0.0.0:1234 ...
connect to 10.2.0.14:1234 from 242.0.255.252:41383 (242.0.255.252:41383)
[dataplane] connector says 7fec4a1e-43ab-433c-baba-20fb7bf1b0bb

STEP: Verifying that the listener got the connector's data and the connector got the listener's data
STEP: Verifying the output of the listener pod contains a namespace-scoped global IP [242.0.255.252] of the connector Pod
STEP: Deleting service "test-svc-tcp-check-listener" on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-h6l6v" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-h6l6v" on cluster "cluster-us-west"
•
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod matching an egress IP pod selector connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-vqhc9" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-vqhc9" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:05:23.085: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says dd055ed7-b1e9-4fe7-839d-eee6f1fe015d; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-vqhc9 PodName:customzm7ph ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c274e5a"
STEP: Waiting for the listener pod "tcp-check-listenerr6wj9" on node "lke109602-163536-646b6c5c35c6" to exit, returning what listener sent
May 22 11:08:23.949: INFO: Pod "tcp-check-listenerr6wj9" on node "lke109602-163536-646b6c5c35c6" output:
listening on 0.0.0.0:1234 ...
nc: timeout

STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-vqhc9" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-vqhc9" on cluster "cluster-us-west"

• Failure [202.176 seconds]
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:28
  when a pod matching an egress IP pod selector connects via TCP to the globalIP of a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:100
    when the pod is not on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:109
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37

      Expected
          <int32>: 1
      to equal
          <int32>: 0

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod matching an egress IP pod selector connects via TCP to the globalIP of a remote service when the pod is on a gateway and the remote service is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-glf4c" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-glf4c" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:08:45.549: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says 3a63cb8e-a5e2-4bac-9157-2e8541346ccd; done | for i in $(seq 2); do if nc -v 242.1.255.252 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-glf4c PodName:customp5ftd ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c270f06"
STEP: Waiting for the listener pod "tcp-check-listenerntld6" on node "lke109602-163536-646b6c5c12e0" to exit, returning what listener sent
May 22 11:08:51.405: INFO: Pod "tcp-check-listenerntld6" on node "lke109602-163536-646b6c5c12e0" output:
listening on 0.0.0.0:1234 ...
connect to 10.2.0.15:1234 from 242.0.255.252:41229 (242.0.255.252:41229)
[dataplane] connector says 3a63cb8e-a5e2-4bac-9157-2e8541346ccd

STEP: Verifying that the listener got the connector's data and the connector got the listener's data
STEP: Verifying the output of the listener pod contains a pod-scoped global IP [242.0.255.252] of the connector Pod
STEP: Deleting service "test-svc-tcp-check-listener" on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-glf4c" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-glf4c" on cluster "cluster-us-west"
•
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod with HostNetworking connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-8qx2k" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-8qx2k" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:09:07.825: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says 9e4e3571-5baf-483d-ba9c-cc14f437e17c; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-8qx2k PodName:customf869b ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c274e5a"
STEP: Waiting for the listener pod "tcp-check-listenerwck9c" on node "lke109602-163536-646b6c5c35c6" to exit, returning what listener sent
May 22 11:12:08.588: INFO: Pod "tcp-check-listenerwck9c" on node "lke109602-163536-646b6c5c35c6" output:
listening on 0.0.0.0:1234 ...
nc: timeout

STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-8qx2k" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-8qx2k" on cluster "cluster-us-west"

• Failure [196.896 seconds]
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:28
  when a pod with HostNetworking connects via TCP to the globalIP of a remote service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:118
    when the pod is not on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:127
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37

      Expected
          <int32>: 1
      to equal
          <int32>: 0

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod with HostNetworking connects via TCP to the globalIP of a remote service when the pod is on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-sb9rj" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-sb9rj" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:12:25.008: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says ea9e454b-faf6-4f7a-98de-ea0c90d8bed7; done | for i in $(seq 2); do if nc -v 242.1.255.252 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-sb9rj PodName:customwzdrb ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c270f06"
STEP: Waiting for the listener pod "tcp-check-listenerjfwbt" on node "lke109602-163536-646b6c5c35c6" to exit, returning what listener sent
May 22 11:12:30.862: INFO: Pod "tcp-check-listenerjfwbt" on node "lke109602-163536-646b6c5c35c6" output:
listening on 0.0.0.0:1234 ...
connect to 10.2.1.25:1234 from 242.0.0.3:41189 (242.0.0.3:41189)
[dataplane] connector says ea9e454b-faf6-4f7a-98de-ea0c90d8bed7

STEP: Verifying that the listener got the connector's data and the connector got the listener's data
STEP: Verifying the output of the listener pod contains a cluster-scoped global IP [242.0.0.1 242.0.0.2 242.0.0.3 242.0.0.4 242.0.0.5 242.0.0.6 242.0.0.7 242.0.0.8] of the connector Pod
STEP: Deleting service "test-svc-tcp-check-listener" on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-sb9rj" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-sb9rj" on cluster "cluster-us-west"
•
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote headless service when the pod is not on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-pz6xw" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-pz6xw" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:12:47.518: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says b2f53978-3e22-4f49-9e32-93f322afaa09; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-pz6xw PodName:customwf6dw ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c274e5a"
STEP: Waiting for the listener pod "tcp-check-listener9t67l" on node "lke109602-163536-646b6c5c35c6" to exit, returning what listener sent
May 22 11:15:48.285: INFO: Pod "tcp-check-listener9t67l" on node "lke109602-163536-646b6c5c35c6" output:
listening on 0.0.0.0:1234 ...
nc: timeout

STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-pz6xw" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-pz6xw" on cluster "cluster-us-west"

• Failure [197.138 seconds]
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:28
  when a pod connects via TCP to the globalIP of a remote headless service
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:136
    when the pod is not on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:145
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37

      Expected
          <int32>: 1
      to equal
          <int32>: 0

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote headless service when the pod is on a gateway and the remote service is on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-xfm68" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-xfm68" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-west", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-west"
STEP: Creating a connector pod in cluster "cluster-us-east", which will attempt the specific UUID handshake over TCP
May 22 11:16:04.796: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says 075046b0-e7bb-48e8-9646-e599610ad459; done | for i in $(seq 2); do if nc -v 242.1.255.253 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-xfm68 PodName:customnb9vz ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109600-163534-646b6c270f06"
STEP: Waiting for the listener pod "tcp-check-listeners9hqm" on node "lke109602-163536-646b6c5c12e0" to exit, returning what listener sent
May 22 11:16:10.652: INFO: Pod "tcp-check-listeners9hqm" on node "lke109602-163536-646b6c5c12e0" output:
listening on 0.0.0.0:1234 ...
connect to 10.2.0.16:1234 from 242.0.0.6:44779 (242.0.0.6:44779)
[dataplane] connector says 075046b0-e7bb-48e8-9646-e599610ad459

STEP: Verifying that the listener got the connector's data and the connector got the listener's data
STEP: Verifying the output of the listener pod contains a cluster-scoped global IP [242.0.0.1 242.0.0.2 242.0.0.3 242.0.0.4 242.0.0.5 242.0.0.6 242.0.0.7 242.0.0.8] of the connector Pod
STEP: Deleting service "test-svc-tcp-check-listener" on "cluster-us-west"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-xfm68" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-xfm68" on cluster "cluster-us-west"
•
------------------------------
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote service in reverse direction when the pod is not on a gateway and the remote service is not on a gateway 
  should have sent the expected data from the pod to the other pod
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37
STEP: Creating namespace objects with basename "dataplane-gn-conn-nd"
STEP: Generated namespace "e2e-tests-dataplane-gn-conn-nd-g6sw6" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-dataplane-gn-conn-nd-g6sw6" in cluster "cluster-us-west"
STEP: Creating a listener pod in cluster "cluster-us-east", which will wait for a handshake over TCP
STEP: Pointing a ClusterIP service to the listener pod in cluster "cluster-us-east"
STEP: Creating a connector pod in cluster "cluster-us-west", which will attempt the specific UUID handshake over TCP
May 22 11:16:22.029: INFO: ExecWithOptions &{Command:[sh -c for j in $(seq 50); do echo [dataplane] connector says c9a1d98f-d2ea-42d8-b151-f7861070214c; done | for i in $(seq 2); do if nc -v 242.0.255.252 1234 -w 60; then break; else sleep 30; fi; done] Namespace:e2e-tests-dataplane-gn-conn-nd-g6sw6 PodName:custommqvln ContainerName:connector-pod Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:true}
STEP: Connector pod is scheduled on node "lke109602-163536-646b6c5c35c6"
STEP: Waiting for the listener pod "tcp-check-listenerfddpl" on node "lke109600-163534-646b6c274e5a" to exit, returning what listener sent
May 22 11:19:22.653: INFO: Pod "tcp-check-listenerfddpl" on node "lke109600-163534-646b6c274e5a" output:
listening on 0.0.0.0:1234 ...
nc: timeout

STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-g6sw6" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-dataplane-gn-conn-nd-g6sw6" on cluster "cluster-us-west"

• Failure [191.794 seconds]
[dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery
github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:28
  when a pod connects via TCP to the globalIP of a remote service in reverse direction
  github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:154
    when the pod is not on a gateway and the remote service is not on a gateway
    github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:163
      should have sent the expected data from the pod to the other pod [It]
      github.com/submariner-io/submariner@v0.14.4/test/e2e/dataplane/tcp_gn_pod_connectivity.go:37

      Expected
          <int32>: 1
      to equal
          <int32>: 0

      github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188
------------------------------
SS
------------------------------
[discovery] Test Service Discovery Across Clusters when a pod tries to resolve a service in a remote cluster 
  should be able to discover the remote service successfully
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:46
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-67bd5" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-67bd5" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on on "cluster-us-west"
STEP: Creating a Nginx Service on "cluster-us-west"
STEP: Creating serviceExport nginx-demo.e2e-tests-discovery-67bd5 on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-demo.e2e-tests-discovery-67bd5 on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Retrieving service nginx-demo.e2e-tests-discovery-67bd5 on "cluster-us-west"
STEP: Retrieving ServiceImport for nginx-demo-e2e-tests-discovery-67bd5- on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-67bd5" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-67bd5" on "cluster-us-east"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify IP "242.1.255.253" for service "nginx-demo" "is" discoverable
May 22 11:19:39.261: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "242.1.255.253" is "242.1.255.253"
STEP: Executing "dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:19:39.886: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 80 nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local." is 80 and the domain name is "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Executing "dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:19:40.508: INFO: ExecWithOptions &{Command:[dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 8183 nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local." is 8183 and the domain name is "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Executing "dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:19:41.424: INFO: ExecWithOptions &{Command:[dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 80 nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local.\n0 50 8183 nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local." is 80 and the domain name is "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Executing "dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:19:42.057: INFO: ExecWithOptions &{Command:[dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 80 nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local.\n0 50 8183 nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local." is 8183 and the domain name is "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Deleting serviceExport nginx-demo.e2e-tests-discovery-67bd5 on "cluster-us-west"
STEP: Deleting service "nginx-demo" on "cluster-us-west"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify IP "" for service "nginx-demo" "is" discoverable
May 22 11:19:47.996: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "" is ""
STEP: Executing "dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is not" discoverable
May 22 11:19:48.623: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "" is not 80 and the domain name is not "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Executing "dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is not" discoverable
May 22 11:19:49.244: INFO: ExecWithOptions &{Command:[dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "" is not 8183 and the domain name is not "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Executing "dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is not" discoverable
May 22 11:19:49.873: INFO: ExecWithOptions &{Command:[dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "" is not 80 and the domain name is not "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Executing "dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is not" discoverable
May 22 11:19:50.493: INFO: ExecWithOptions &{Command:[dig +short SRV nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local] Namespace:e2e-tests-discovery-67bd5 PodName:netshootdh6xv-6898dd765f-q7jpc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "" is not 8183 and the domain name is not "nginx-demo.e2e-tests-discovery-67bd5.svc.clusterset.local"
STEP: Deleting namespace "e2e-tests-discovery-67bd5" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-67bd5" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-67bd5" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-67bd5" on "cluster-us-east"
•
------------------------------
[discovery] Test Service Discovery Across Clusters when a pod tries to resolve a service which is present locally and in a remote cluster 
  should resolve the local service
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:52
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-nm2vx" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-nm2vx" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-east"
STEP: Creating a Nginx Service on "cluster-us-east"
STEP: Creating an Nginx Deployment on "cluster-us-west"
STEP: Creating a Nginx Service on "cluster-us-west"
STEP: Creating serviceExport nginx-demo.e2e-tests-discovery-nm2vx on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-demo.e2e-tests-discovery-nm2vx on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
May 22 11:20:12.476: INFO: ExecWithOptions &{Command:[cat /etc/resolv.conf] Namespace:e2e-tests-discovery-nm2vx PodName:netshootmmrwr-6898dd765f-27zcw ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-nm2vx.svc.cluster.local" to verify IP "10.128.168.5" for service "nginx-demo" "is" discoverable
May 22 11:20:13.104: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-nm2vx.svc.cluster.local] Namespace:e2e-tests-discovery-nm2vx PodName:netshootmmrwr-6898dd765f-27zcw ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "10.128.168.5" is "10.128.168.5"
STEP: Deleting service "nginx-demo" on "cluster-us-east"
STEP: Retrieving service nginx-demo.e2e-tests-discovery-nm2vx on "cluster-us-west"
STEP: Retrieving ServiceImport for nginx-demo-e2e-tests-discovery-nm2vx- on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-nm2vx" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-nm2vx" on "cluster-us-east"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-nm2vx.svc.clusterset.local" to verify IP "242.1.255.253" for service "nginx-demo" "is" discoverable
May 22 11:20:14.204: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-nm2vx.svc.clusterset.local] Namespace:e2e-tests-discovery-nm2vx PodName:netshootmmrwr-6898dd765f-27zcw ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "242.1.255.253" is "242.1.255.253"
STEP: Deleting serviceExport nginx-demo.e2e-tests-discovery-nm2vx on "cluster-us-west"
STEP: Deleting service "nginx-demo" on "cluster-us-west"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-nm2vx.svc.clusterset.local" to verify IP "" for service "nginx-demo" "is" discoverable
May 22 11:20:20.108: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-nm2vx.svc.clusterset.local] Namespace:e2e-tests-discovery-nm2vx PodName:netshootmmrwr-6898dd765f-27zcw ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "" is ""
STEP: Deleting namespace "e2e-tests-discovery-nm2vx" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-nm2vx" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-nm2vx" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-nm2vx" on "cluster-us-east"
•
------------------------------
[discovery] Test Service Discovery Across Clusters when service export is created before the service 
  should resolve the service
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:58
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-7vrw9" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-7vrw9" in cluster "cluster-us-west"
STEP: Creating an Nginx ServiceExport on "cluster-us-west"
STEP: Creating serviceExport nginx-demo.e2e-tests-discovery-7vrw9 on "cluster-us-west"
STEP: Creating an Nginx Deployment on on "cluster-us-west"
STEP: Creating a Nginx Service on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Retrieving service nginx-demo.e2e-tests-discovery-7vrw9 on "cluster-us-west"
STEP: Retrieving ServiceImport for nginx-demo-e2e-tests-discovery-7vrw9- on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-7vrw9" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-7vrw9" on "cluster-us-east"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-7vrw9.svc.clusterset.local" to verify IP "242.1.255.253" for service "nginx-demo" "is" discoverable
May 22 11:20:31.941: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-7vrw9.svc.clusterset.local] Namespace:e2e-tests-discovery-7vrw9 PodName:netshootzcxt8-6898dd765f-5c5cs ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "242.1.255.253" is "242.1.255.253"
STEP: Deleting serviceExport nginx-demo.e2e-tests-discovery-7vrw9 on "cluster-us-west"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-7vrw9.svc.clusterset.local" to verify IP "" for service "nginx-demo" "is" discoverable
May 22 11:20:37.772: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-7vrw9.svc.clusterset.local] Namespace:e2e-tests-discovery-7vrw9 PodName:netshootzcxt8-6898dd765f-5c5cs ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "" is ""
STEP: Deleting namespace "e2e-tests-discovery-7vrw9" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-7vrw9" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-7vrw9" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-7vrw9" on "cluster-us-east"
•
------------------------------
[discovery] Test Service Discovery Across Clusters when there are no active pods for a service 
  should not resolve the service
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:63
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-z6v95" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-z6v95" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on on "cluster-us-west"
STEP: Creating a Nginx Service on "cluster-us-west"
STEP: Creating serviceExport nginx-demo.e2e-tests-discovery-z6v95 on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-demo.e2e-tests-discovery-z6v95 on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Retrieving service nginx-demo.e2e-tests-discovery-z6v95 on "cluster-us-west"
STEP: Retrieving ServiceImport for nginx-demo-e2e-tests-discovery-z6v95- on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-z6v95" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-z6v95" on "cluster-us-east"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify IP "242.1.255.253" for service "nginx-demo" "is" discoverable
May 22 11:20:54.764: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "242.1.255.253" is "242.1.255.253"
STEP: Executing "dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:20:55.445: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 80 nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local." is 80 and the domain name is "nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local"
STEP: Executing "dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:20:56.108: INFO: ExecWithOptions &{Command:[dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 8183 nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local." is 8183 and the domain name is "nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local"
STEP: Setting Nginx deployment replicas to 0 in cluster "cluster-us-west"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify IP "242.1.255.253" for service "nginx-demo" "is not" discoverable
May 22 11:20:56.828: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "" is not "242.1.255.253"
STEP: Executing "dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is not" discoverable
May 22 11:20:57.512: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "" is not 80 and the domain name is not "nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local"
STEP: Executing "dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is not" discoverable
May 22 11:20:58.128: INFO: ExecWithOptions &{Command:[dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "" is not 8183 and the domain name is not "nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local"
STEP: Setting Nginx deployment replicas to 2 in cluster "cluster-us-west"
STEP: Executing "dig +short nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify IP "242.1.255.253" for service "nginx-demo" "is" discoverable
May 22 11:20:58.844: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "" is "242.1.255.253"
May 22 11:21:04.479: INFO: ExecWithOptions &{Command:[dig +short nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "242.1.255.253" is "242.1.255.253"
STEP: Executing "dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:21:05.188: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 80 nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local." is 80 and the domain name is "nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local"
STEP: Executing "dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:21:05.814: INFO: ExecWithOptions &{Command:[dig +short SRV metrics.tcp.nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local] Namespace:e2e-tests-discovery-z6v95 PodName:netshootkhf9f-6898dd765f-b45bh ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 8183 nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local." is 8183 and the domain name is "nginx-demo.e2e-tests-discovery-z6v95.svc.clusterset.local"
STEP: Deleting namespace "e2e-tests-discovery-z6v95" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-z6v95" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-z6v95" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-z6v95" on "cluster-us-east"
•
------------------------------
[discovery] Test Service Discovery Across Clusters when there are active pods for a service in only one cluster 
  should not resolve the service on the cluster without active pods
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:69
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-62c7n" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-62c7n" in cluster "cluster-us-west"
STEP: Deleting namespace "e2e-tests-discovery-62c7n" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-62c7n" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-62c7n" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-62c7n" on "cluster-us-east"

S [SKIPPING] [0.388 seconds]
[discovery] Test Service Discovery Across Clusters
github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:42
  when there are active pods for a service in only one cluster
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:68
    should not resolve the service on the cluster without active pods [It]
    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:69

    Only two clusters are deployed and hence skipping the test

    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:293
------------------------------
[discovery] Test Service Discovery Across Clusters when a pod tries to resolve a service in a specific remote cluster by its cluster name 
  should resolve the service on the specified cluster
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:75
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-7ppd5" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-7ppd5" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-east"
STEP: Creating a Nginx Service on "cluster-us-east"
STEP: Creating serviceExport nginx-demo.e2e-tests-discovery-7ppd5 on "cluster-us-east"
STEP: Creating an Nginx Deployment on "cluster-us-west"
STEP: Creating a Nginx Service on "cluster-us-west"
STEP: Creating serviceExport nginx-demo.e2e-tests-discovery-7ppd5 on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-demo.e2e-tests-discovery-7ppd5 on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Retrieving service nginx-demo.e2e-tests-discovery-7ppd5 on "cluster-us-east"
STEP: Retrieving ServiceImport for nginx-demo-e2e-tests-discovery-7ppd5- on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-7ppd5" on "cluster-us-east"
STEP: Executing "dig +short cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local" to verify IP "10.128.155.207" for service "nginx-demo" "is" discoverable
May 22 11:21:38.781: INFO: ExecWithOptions &{Command:[dig +short cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local] Namespace:e2e-tests-discovery-7ppd5 PodName:netshootmdtlr-6898dd765f-4677s ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "10.128.155.207" is "10.128.155.207"
STEP: Executing "dig +short SRV http.tcp.cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:21:39.421: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local] Namespace:e2e-tests-discovery-7ppd5 PodName:netshootmdtlr-6898dd765f-4677s ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 80 cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local." is 80 and the domain name is "cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local"
STEP: Executing "dig +short SRV metrics.tcp.cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:21:40.039: INFO: ExecWithOptions &{Command:[dig +short SRV metrics.tcp.cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local] Namespace:e2e-tests-discovery-7ppd5 PodName:netshootmdtlr-6898dd765f-4677s ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 8183 cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local." is 8183 and the domain name is "cluster-us-east.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local"
STEP: Retrieving service nginx-demo.e2e-tests-discovery-7ppd5 on "cluster-us-west"
STEP: Retrieving ServiceImport for nginx-demo-e2e-tests-discovery-7ppd5- on "cluster-us-east"
STEP: Retrieving EndpointSlices for "nginx-demo" in ns "e2e-tests-discovery-7ppd5" on "cluster-us-west"
STEP: Executing "dig +short cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local" to verify IP "242.1.255.253" for service "nginx-demo" "is" discoverable
May 22 11:21:40.892: INFO: ExecWithOptions &{Command:[dig +short cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local] Namespace:e2e-tests-discovery-7ppd5 PodName:netshootmdtlr-6898dd765f-4677s ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result "242.1.255.253" is "242.1.255.253"
STEP: Executing "dig +short SRV http.tcp.cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:21:41.517: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local] Namespace:e2e-tests-discovery-7ppd5 PodName:netshootmdtlr-6898dd765f-4677s ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 80 cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local." is 80 and the domain name is "cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local"
STEP: Executing "dig +short SRV metrics.tcp.cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local" to verify SRV record for service "nginx-demo" "is" discoverable
May 22 11:21:42.141: INFO: ExecWithOptions &{Command:[dig +short SRV metrics.tcp.cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local] Namespace:e2e-tests-discovery-7ppd5 PodName:netshootmdtlr-6898dd765f-4677s ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that port in dig result for SRV Record "0 50 8183 cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local." is 8183 and the domain name is "cluster-us-west.nginx-demo.e2e-tests-discovery-7ppd5.svc.clusterset.local"
STEP: Deleting namespace "e2e-tests-discovery-7ppd5" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-7ppd5" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-7ppd5" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-7ppd5" on "cluster-us-east"
•
------------------------------
[discovery] Test Service Discovery Across Clusters when a pod tries to resolve a service multiple times 
  should resolve the service from both the clusters in a round robin fashion
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:81
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-8mcfw" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-8mcfw" in cluster "cluster-us-west"
STEP: Deleting namespace "e2e-tests-discovery-8mcfw" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-8mcfw" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-8mcfw" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-8mcfw" on "cluster-us-east"

S [SKIPPING] [0.364 seconds]
[discovery] Test Service Discovery Across Clusters
github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:42
  when a pod tries to resolve a service multiple times
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:80
    should resolve the service from both the clusters in a round robin fashion [It]
    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:81

    Only two clusters are deployed and hence skipping the test

    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:415
------------------------------
[discovery] Test Service Discovery Across Clusters when one of the clusters with a service is not healthy 
  should not resolve that cluster's service IP
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:106
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-s62cz" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-s62cz" in cluster "cluster-us-west"
STEP: Deleting namespace "e2e-tests-discovery-s62cz" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-s62cz" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-s62cz" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-s62cz" on "cluster-us-east"

S [SKIPPING] in Spec Setup (BeforeEach) [0.415 seconds]
[discovery] Test Service Discovery Across Clusters
github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:42
  when one of the clusters with a service is not healthy
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:86
    should not resolve that cluster's service IP [BeforeEach]
    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:106

    Only two clusters are deployed and hence skipping the test

    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/service_discovery.go:91
------------------------------
[discovery] Test Headless Service Discovery Across Clusters when a pod tries to resolve a headless service in a remote cluster 
  should resolve the backing pod IPs from the remote cluster
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:41
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-9sl6m" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-9sl6m" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-west"
STEP: Creating a Nginx Headless Service on "cluster-us-west"
STEP: Creating serviceExport nginx-headless.e2e-tests-discovery-9sl6m on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-headless.e2e-tests-discovery-9sl6m on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-headless" "are" discoverable
May 22 11:22:09.982: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local] Namespace:e2e-tests-discovery-9sl6m PodName:netshoot78c77-6898dd765f-nqkzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253"
STEP: Executing "dig +short cluster-us-west.nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-headless" "are" discoverable
May 22 11:22:10.654: INFO: ExecWithOptions &{Command:[dig +short cluster-us-west.nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local] Namespace:e2e-tests-discovery-9sl6m PodName:netshoot78c77-6898dd765f-nqkzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253"
STEP: Executing "dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-n9bm5] for service "nginx-headless" "are" discoverable
May 22 11:22:11.277: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local] Namespace:e2e-tests-discovery-9sl6m PodName:netshoot78c77-6898dd765f-nqkzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-n9bm5.cluster-us-west.nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local."
STEP: Executing "dig +short SRV nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-n9bm5] for service "nginx-headless" "are" discoverable
May 22 11:22:11.906: INFO: ExecWithOptions &{Command:[dig +short SRV nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local] Namespace:e2e-tests-discovery-9sl6m PodName:netshoot78c77-6898dd765f-nqkzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-n9bm5.cluster-us-west.nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local."
STEP: Deleting serviceExport nginx-headless.e2e-tests-discovery-9sl6m on "cluster-us-west"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-headless" "are not" discoverable
May 22 11:22:17.756: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local] Namespace:e2e-tests-discovery-9sl6m PodName:netshoot78c77-6898dd765f-nqkzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Executing "dig +short SRV nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-n9bm5] for service "nginx-headless" "are not" discoverable
May 22 11:22:18.380: INFO: ExecWithOptions &{Command:[dig +short SRV nginx-headless.e2e-tests-discovery-9sl6m.svc.clusterset.local] Namespace:e2e-tests-discovery-9sl6m PodName:netshoot78c77-6898dd765f-nqkzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Deleting namespace "e2e-tests-discovery-9sl6m" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-9sl6m" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-9sl6m" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-9sl6m" on "cluster-us-east"
•
------------------------------
[discovery] Test Headless Service Discovery Across Clusters when a pod tries to resolve a headless service which is exported locally and in a remote cluster 
  should resolve the backing pod IPs from both clusters
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:47
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-6dgdg" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-6dgdg" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-west"
STEP: Creating a Nginx Headless Service on "cluster-us-west"
STEP: Creating serviceExport nginx-headless.e2e-tests-discovery-6dgdg on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-headless.e2e-tests-discovery-6dgdg on "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-east"
STEP: Creating a Nginx Headless Service on "cluster-us-east"
STEP: Creating serviceExport nginx-headless.e2e-tests-discovery-6dgdg on "cluster-us-east"
STEP: Retrieving ServiceExport nginx-headless.e2e-tests-discovery-6dgdg on "cluster-us-east"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local" to verify IPs [242.1.255.253 10.2.2.30] for service "nginx-headless" "are" discoverable
May 22 11:23:21.164: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local] Namespace:e2e-tests-discovery-6dgdg PodName:netshootgmbtk-6898dd765f-4bw6l ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253\n10.2.2.30"
STEP: Executing "dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-vvl7g] for service "nginx-headless" "are" discoverable
May 22 11:23:21.797: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local] Namespace:e2e-tests-discovery-6dgdg PodName:netshootgmbtk-6898dd765f-4bw6l ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-vvl7g.cluster-us-west.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local.\n0 50 80 nginx-demo-f58797fd9-6ncbt.cluster-us-east.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local."
STEP: Executing "dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-6ncbt] for service "nginx-headless" "are" discoverable
May 22 11:23:22.512: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local] Namespace:e2e-tests-discovery-6dgdg PodName:netshootgmbtk-6898dd765f-4bw6l ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-vvl7g.cluster-us-west.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local.\n0 50 80 nginx-demo-f58797fd9-6ncbt.cluster-us-east.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local."
STEP: Deleting serviceExport nginx-headless.e2e-tests-discovery-6dgdg on "cluster-us-west"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-headless" "are not" discoverable
May 22 11:23:28.364: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local] Namespace:e2e-tests-discovery-6dgdg PodName:netshootgmbtk-6898dd765f-4bw6l ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "10.2.2.30"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local" to verify IPs [10.2.2.30] for service "nginx-headless" "are" discoverable
May 22 11:23:28.996: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local] Namespace:e2e-tests-discovery-6dgdg PodName:netshootgmbtk-6898dd765f-4bw6l ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "10.2.2.30"
STEP: Executing "dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-vvl7g] for service "nginx-headless" "are not" discoverable
May 22 11:23:29.641: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local] Namespace:e2e-tests-discovery-6dgdg PodName:netshootgmbtk-6898dd765f-4bw6l ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not "0 50 80 nginx-demo-f58797fd9-6ncbt.cluster-us-east.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local."
STEP: Executing "dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-6ncbt] for service "nginx-headless" "are" discoverable
May 22 11:23:30.250: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local] Namespace:e2e-tests-discovery-6dgdg PodName:netshootgmbtk-6898dd765f-4bw6l ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-6ncbt.cluster-us-east.nginx-headless.e2e-tests-discovery-6dgdg.svc.clusterset.local."
STEP: Deleting namespace "e2e-tests-discovery-6dgdg" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-6dgdg" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-6dgdg" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-6dgdg" on "cluster-us-east"

• [SLOW TEST:81.845 seconds]
[discovery] Test Headless Service Discovery Across Clusters
github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:37
  when a pod tries to resolve a headless service which is exported locally and in a remote cluster
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:46
    should resolve the backing pod IPs from both clusters
    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:47
------------------------------
[discovery] Test Headless Service Discovery Across Clusters when the number of active pods backing a service changes 
  should only resolve the IPs from the active pods
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:53
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-gdxv9" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-gdxv9" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-west"
STEP: Setting Nginx deployment replicas to 3 in cluster "cluster-us-west"
STEP: Creating a Nginx Headless Service on "cluster-us-west"
STEP: Creating serviceExport nginx-headless.e2e-tests-discovery-gdxv9 on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-headless.e2e-tests-discovery-gdxv9 on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-gdxv9.svc.clusterset.local" to verify IPs [242.1.255.253 242.1.255.251 242.1.255.252] for service "nginx-headless" "are" discoverable
May 22 11:23:57.284: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-gdxv9.svc.clusterset.local] Namespace:e2e-tests-discovery-gdxv9 PodName:netshootd9q6p-6898dd765f-cgjq8 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.251\n242.1.255.253\n242.1.255.252"
STEP: Setting Nginx deployment replicas to 0 in cluster "cluster-us-west"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-gdxv9.svc.clusterset.local" to verify IPs [] for service "nginx-headless" "are not" discoverable
May 22 11:24:33.068: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-gdxv9.svc.clusterset.local] Namespace:e2e-tests-discovery-gdxv9 PodName:netshootd9q6p-6898dd765f-cgjq8 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Setting Nginx deployment replicas to 2 in cluster "cluster-us-west"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-gdxv9.svc.clusterset.local" to verify IPs [242.1.255.252 242.1.255.253] for service "nginx-headless" "are" discoverable
May 22 11:24:38.900: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-gdxv9.svc.clusterset.local] Namespace:e2e-tests-discovery-gdxv9 PodName:netshootd9q6p-6898dd765f-cgjq8 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.252\n242.1.255.253"
STEP: Deleting namespace "e2e-tests-discovery-gdxv9" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-gdxv9" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-gdxv9" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-gdxv9" on "cluster-us-east"

• [SLOW TEST:68.587 seconds]
[discovery] Test Headless Service Discovery Across Clusters
github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:37
  when the number of active pods backing a service changes
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:52
    should only resolve the IPs from the active pods
    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:53
------------------------------
[discovery] Test Headless Service Discovery Across Clusters when the number of active pods backing a service changes 
  should resolve the local pod IPs
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:57
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-zvhpp" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-zvhpp" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-east"
STEP: Setting Nginx deployment replicas to 3 in cluster "cluster-us-east"
STEP: Creating a Nginx Headless Service on "cluster-us-east"
STEP: Creating serviceExport nginx-headless.e2e-tests-discovery-zvhpp on "cluster-us-east"
STEP: Retrieving ServiceExport nginx-headless.e2e-tests-discovery-zvhpp on "cluster-us-east"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-zvhpp.svc.clusterset.local" to verify IPs [10.2.1.25 10.2.2.32 10.2.0.7] for service "nginx-headless" "are" discoverable
May 22 11:25:06.476: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-zvhpp.svc.clusterset.local] Namespace:e2e-tests-discovery-zvhpp PodName:netshoot2vn2c-6898dd765f-d5vzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "10.2.0.7\n10.2.1.25\n10.2.2.32"
STEP: Setting Nginx deployment replicas to 0 in cluster "cluster-us-east"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-zvhpp.svc.clusterset.local" to verify IPs [] for service "nginx-headless" "are not" discoverable
May 22 11:25:42.476: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-zvhpp.svc.clusterset.local] Namespace:e2e-tests-discovery-zvhpp PodName:netshoot2vn2c-6898dd765f-d5vzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are not ""
STEP: Setting Nginx deployment replicas to 2 in cluster "cluster-us-east"
STEP: Executing "dig +short nginx-headless.e2e-tests-discovery-zvhpp.svc.clusterset.local" to verify IPs [10.2.2.34 10.2.1.26] for service "nginx-headless" "are" discoverable
May 22 11:25:48.572: INFO: ExecWithOptions &{Command:[dig +short nginx-headless.e2e-tests-discovery-zvhpp.svc.clusterset.local] Namespace:e2e-tests-discovery-zvhpp PodName:netshoot2vn2c-6898dd765f-d5vzc ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "10.2.1.26\n10.2.2.34"
STEP: Deleting namespace "e2e-tests-discovery-zvhpp" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-zvhpp" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-zvhpp" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-zvhpp" on "cluster-us-east"

• [SLOW TEST:69.696 seconds]
[discovery] Test Headless Service Discovery Across Clusters
github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:37
  when the number of active pods backing a service changes
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:52
    should resolve the local pod IPs
    github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:57
------------------------------
[discovery] Test Headless Service Discovery Across Clusters when a pod tries to resolve a headless service in a specific remote cluster by its cluster name 
  should resolve the backing pod IPs from the specified remote cluster
  github.com/submariner-io/lighthouse@v0.14.4/test/e2e/discovery/headless_services.go:63
STEP: Creating namespace objects with basename "discovery"
STEP: Generated namespace "e2e-tests-discovery-nw88s" in cluster "cluster-us-east" to execute the tests in
STEP: Creating namespace "e2e-tests-discovery-nw88s" in cluster "cluster-us-west"
STEP: Creating an Nginx Deployment on "cluster-us-east"
STEP: Creating a Nginx Headless Service on "cluster-us-east"
STEP: Creating serviceExport nginx-headless.e2e-tests-discovery-nw88s on "cluster-us-east"
STEP: Retrieving ServiceExport nginx-headless.e2e-tests-discovery-nw88s on "cluster-us-east"
STEP: Creating an Nginx Deployment on "cluster-us-west"
STEP: Creating a Nginx Headless Service on "cluster-us-west"
STEP: Creating serviceExport nginx-headless.e2e-tests-discovery-nw88s on "cluster-us-west"
STEP: Retrieving ServiceExport nginx-headless.e2e-tests-discovery-nw88s on "cluster-us-west"
STEP: Creating a Netshoot Deployment on "cluster-us-east"
STEP: Executing "dig +short cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local" to verify IPs [10.2.1.27] for service "nginx-headless" "are" discoverable
May 22 11:26:26.156: INFO: ExecWithOptions &{Command:[dig +short cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local] Namespace:e2e-tests-discovery-nw88s PodName:netshootj4zxh-6898dd765f-fr5q6 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "10.2.1.27"
STEP: Executing "dig +short cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local" to verify IPs [242.1.255.253] for service "nginx-headless" "are" discoverable
May 22 11:26:27.309: INFO: ExecWithOptions &{Command:[dig +short cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local] Namespace:e2e-tests-discovery-nw88s PodName:netshootj4zxh-6898dd765f-fr5q6 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "242.1.255.253"
STEP: Executing "dig +short SRV http.tcp.cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-gm7tb] for service "nginx-headless" "are" discoverable
May 22 11:26:27.932: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local] Namespace:e2e-tests-discovery-nw88s PodName:netshootj4zxh-6898dd765f-fr5q6 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-gm7tb.cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local."
STEP: Executing "dig +short SRV http.tcp.cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-mnsj5] for service "nginx-headless" "are" discoverable
May 22 11:26:28.556: INFO: ExecWithOptions &{Command:[dig +short SRV http.tcp.cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local] Namespace:e2e-tests-discovery-nw88s PodName:netshootj4zxh-6898dd765f-fr5q6 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-mnsj5.cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local."
STEP: Executing "dig +short SRV cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-gm7tb] for service "nginx-headless" "are" discoverable
May 22 11:26:29.184: INFO: ExecWithOptions &{Command:[dig +short SRV cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local] Namespace:e2e-tests-discovery-nw88s PodName:netshootj4zxh-6898dd765f-fr5q6 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-gm7tb.cluster-us-east.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local."
STEP: Executing "dig +short SRV cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local" to verify hostNames [nginx-demo-f58797fd9-mnsj5] for service "nginx-headless" "are" discoverable
May 22 11:26:29.815: INFO: ExecWithOptions &{Command:[dig +short SRV cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local] Namespace:e2e-tests-discovery-nw88s PodName:netshootj4zxh-6898dd765f-fr5q6 ContainerName:netshoot Stdin:<nil> CaptureStdout:true CaptureStderr:true PreserveWhitespace:false}
STEP: Validating that dig result are "0 50 80 nginx-demo-f58797fd9-mnsj5.cluster-us-west.nginx-headless.e2e-tests-discovery-nw88s.svc.clusterset.local."
STEP: Deleting namespace "e2e-tests-discovery-nw88s" on cluster "cluster-us-east"
STEP: Deleting namespace "e2e-tests-discovery-nw88s" on cluster "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-nw88s" on "cluster-us-west"
STEP: Retrieving EndpointSlices for "" in ns "e2e-tests-discovery-nw88s" on "cluster-us-east"
•

Summarizing 6 Failures:

[Fail] [dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway [It] should have sent the expected data from the pod to the other pod 
github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188

[Fail] [dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod matching an egress IP namespace selector connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway [It] should have sent the expected data from the pod to the other pod 
github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188

[Fail] [dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod matching an egress IP pod selector connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway [It] should have sent the expected data from the pod to the other pod 
github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188

[Fail] [dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod with HostNetworking connects via TCP to the globalIP of a remote service when the pod is not on a gateway and the remote service is not on a gateway [It] should have sent the expected data from the pod to the other pod 
github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188

[Fail] [dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote headless service when the pod is not on a gateway and the remote service is not on a gateway [It] should have sent the expected data from the pod to the other pod 
github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188

[Fail] [dataplane-globalnet] Basic TCP connectivity tests across overlapping clusters without discovery when a pod connects via TCP to the globalIP of a remote service in reverse direction when the pod is not on a gateway and the remote service is not on a gateway [It] should have sent the expected data from the pod to the other pod 
github.com/submariner-io/shipyard@v0.14.4/test/e2e/framework/network_pods.go:188

Ran 26 of 44 Specs in 1885.803 seconds
FAIL! -- 20 Passed | 6 Failed | 0 Pending | 18 Skipped

subctl version: v0.14.4

```
