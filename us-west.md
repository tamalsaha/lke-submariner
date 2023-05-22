```
$ calicoctl get ippools -o wide --allow-version-mismatch
NAME                  CIDR           NAT     IPIPMODE   VXLANMODE   DISABLED   DISABLEBGPEXPORT   SELECTOR   
default-ipv4-ippool   10.2.0.0/16    true    Always     Never       false      false              all()      
globaleastcluster     242.0.0.0/16   false   Never      Never       true       false              all()      

$ subctl diagnose all
Cluster "lke109602"
 ✓ Checking Submariner support for the Kubernetes version
 ✓ Kubernetes version "v1.26.3" is supported

 ✓ Checking Submariner support for the CNI network plugin
 ✓ The detected CNI network plugin ("calico") is supported
 ✓ Trying to detect the Calico ConfigMap
 ✓ Calico CNI detected, checking if the Submariner IPPool pre-requisites are configured
 ✓ Checking gateway connections
 ✓ All connections are established
 ✓ Globalnet deployment detected - checking if globalnet CIDRs overlap
 ✓ Clusters do not have overlapping globalnet CIDRs
 ✓ Checking Submariner pods 
 ✓ All Submariner pods are up and running
 ✓ Checking if gateway metrics are accessible from non-gateway nodes 
 ✓ The gateway metrics are accessible
 ✓ Checking if globalnet metrics are accessible from non-gateway nodes 
 ✓ The globalnet metrics are accessible
 ✓ Checking Submariner support for the kube-proxy mode 
 ✓ The kube-proxy mode is supported
 ✓ Checking the firewall configuration to determine if intra-cluster VXLAN traffic is allowed 
 ✓ The firewall configuration allows intra-cluster VXLAN traffic
 ✓ Checking Globalnet configuration 
 ✓ Globalnet is properly configured and functioning

 ✓ Checking if services have been exported properly
 ✓ All services have been exported properly


Skipping inter-cluster firewall check as it requires two kubeconfigs. Please run "subctl diagnose firewall inter-cluster" command manually.

$ subctl show all
Cluster "lke109602"
 ✓ Detecting broker(s)
 ✓ No brokers found

 ✓ Showing Connections
GATEWAY                         CLUSTER           REMOTE IP       NAT   CABLE DRIVER   SUBNETS        STATUS      RTT avg.      
lke109600-163534-646b6c270f06   cluster-us-east   104.200.31.80   no    libreswan      242.0.0.0/16   connected   69.923615ms   

 ✓ Showing Endpoints
CLUSTER           ENDPOINT IP     PUBLIC IP       CABLE DRIVER   TYPE     
cluster-us-west   23.239.3.112    23.239.3.112    libreswan      local    
cluster-us-east   104.200.31.80   104.200.31.80   libreswan      remote   

 ✓ Showing Gateways
NODE                            HA STATUS   SUMMARY                               
lke109602-163536-646b6c5c12e0   active      All connections (1) are established   

 ✓ Showing Network details
    Discovered network details via Submariner:
        Network plugin:  calico
        Service CIDRs:   [10.128.0.0/16]
        Cluster CIDRs:   [10.2.0.0/24]
        Global CIDR:     242.1.0.0/16

 ✓ Showing versions 
COMPONENT                       REPOSITORY           VERSION   
submariner-gateway              quay.io/submariner   0.14.4    
submariner-routeagent           quay.io/submariner   0.14.4    
submariner-globalnet            quay.io/submariner   0.14.4    
submariner-operator             quay.io/submariner   0.14.4    
submariner-lighthouse-agent     quay.io/submariner   0.14.4    
submariner-lighthouse-coredns   quay.io/submariner   0.14.4    


$ subctl gather
Cluster "lke109602"
Gathering information from cluster "lke109602"
 ✓ Gathering operator logs 
 ✓ Found 1 pods matching label selector "name=submariner-operator"
 ✓ Gathering operator resources 
 ✓ Found 1 submariners in namespace "submariner-operator"
 ✓ Found 1 servicediscoveries in namespace "submariner-operator"
 ✓ Found 1 deployments by field selector "metadata.name=submariner-operator" in namespace "submariner-operator"
 ✓ Found 1 daemonsets by label selector "app=submariner-gateway" in namespace "submariner-operator"
 ✓ Found 1 daemonsets by label selector "app=submariner-routeagent" in namespace "submariner-operator"
 ✓ Found 1 daemonsets by label selector "app=submariner-globalnet" in namespace "submariner-operator"
 ✓ Found 0 deployments by label selector "app=submariner-networkplugin-syncer" in namespace "submariner-operator"
 ✓ Found 1 deployments by label selector "app=submariner-lighthouse-agent" in namespace "submariner-operator"
 ✓ Found 1 deployments by label selector "app=submariner-lighthouse-coredns" in namespace "submariner-operator"
 ✓ Gathering connectivity logs 
 ✓ Found 1 pods matching label selector "app=submariner-gateway"
 ✓ Found 3 pods matching label selector "app=submariner-routeagent"
 ✓ Found 1 pods matching label selector "app=submariner-globalnet"
 ✓ Found 0 pods matching label selector "app=submariner-networkplugin-syncer"
 ✓ Found 0 pods matching label selector "app=submariner-addon"
 ✓ Gathering connectivity resources 
 ✓ Gathering CNI data from 3 pods matching label selector "app=submariner-routeagent"
 ✓ Gathering CNI data from 1 pods matching label selector "app=submariner-gateway"
 ✓ Gathering cable driver data from 1 pods matching label selector "app=submariner-gateway"
 ✓ Found 2 endpoints in namespace "submariner-operator"
 ✓ Found 2 clusters in namespace "submariner-operator"
 ✓ Found 1 gateways in namespace "submariner-operator"
 ✓ Found 1 clusterglobalegressips in namespace ""
 ✓ Found 0 globalegressips in namespace ""
 ✓ Found 0 globalingressips in namespace ""
 ✓ Gathering service-discovery logs 
 ✓ Found 3 pods matching label selector "component=submariner-lighthouse"
 ✓ Found 2 pods matching label selector "k8s-app=kube-dns"
 ✓ Gathering service-discovery resources 
 ✓ Found 0 serviceexports in namespace ""
 ✓ Found 0 serviceimports in namespace ""
 ✓ Found 0 endpointslices by label selector "endpointslice.kubernetes.io/managed-by=lighthouse-agent.submariner.io" in namespace ""
 ✓ Found 1 configmaps by label selector "component=submariner-lighthouse" in namespace "submariner-operator"
 ✓ Found 1 configmaps by field selector "metadata.name=coredns" in namespace "kube-system"
 ✓ Found 0 services by label selector "submariner.io/exportedServiceRef" in namespace ""
 ✓ Gathering broker logs
 ✓ Gathering broker resources 
 ✓ Found 2 endpoints in namespace "submariner-k8s-broker"
 ✓ Found 2 clusters in namespace "submariner-k8s-broker"
 ✓ Found 0 endpointslices by label selector "endpointslice.kubernetes.io/managed-by=lighthouse-agent.submariner.io" in namespace "submariner-k8s-broker"
 ✓ Found 0 serviceimports in namespace "submariner-k8s-broker"
Files are stored under directory "submariner-20230522134924/lke109602"

```
