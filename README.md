# kubernetes interview quesions!!!

1) What is Kubernetes and why is kubernetes needed ?

2) What are the alternatives to Kubernetes ?

3) Is kubernetes as openSource Orchestrator ? Do we have any paid versions of Kubernetes ?

4) What are some of the famous on-prem editions of Kubernetes ?

5) What is Kubectl and why we need to this ?  What is Kube config and where it will be stored ?

6) What is Data Plane and Control Plane in Kubernetes ?

7) What is KubeAPI Server in kubernetes ?

8) What is a nameSpace in kubernetes ? 

9) What are the default nameSpaces that comes up as apart of the Kubernetes installation ?

10) What is Kube Content vs Current Context ?

11) If you have multiple kubernets clusters, how we switch between them ?

12) What is kube-controller and what's the user of it ?

13) What is Kube-Api Server and what's the user of it ?

14) What's the port number that we use to connec to kubernetes ?

15) What is Regional vs Zonal vs Multi-Zonal Kubernetes Cluster ?

16) What will happen to the workLoads that are running on the Kubernets Cluster,when the Control Pane Node is down ?

17) Can we keep multiple Master Nodes or Control Nodes In A Kubernetes Cluster ?

18) What is Public vs Private Kubernetes Cluster ?

19) What is the current version of Kubernetes ?

20) What is a Managed Kubernetes Cluster in Cloud vs On-Prem Kubernetes Cluster ?

21) In Managed Kuberneetes Cluster, do we have control on the versions of Kube API Server, Kube Scheduler, ETCD Database ?

22) How do you upgrade / update your kubernetes cluster ?

23) What do we update first ? Master Node or the Node Pools? 

24) What is a Nodepool or NodeGroup in Kubermetes ?

25) How do your provision a cluster with t3.large, c3.medium and e2.large servers in your kubernets cluster ?

26) How can we capture the logs of your kubernets cluster and where can we store them to stream the logs whenever we want ?

27) What is OIDC on AWS EKS Cluster ?

28) What is fargate profile on AWS EKS ?

29) What is the Networking Soluton User on AWS EKS ?

30) What is the Container CNI and which Container CNI is used on EKS ?

31) How to capture the KubeAPI, Schedule logs in kubernetes ?

32) What is a Quota or Resoruce Quota in Kuberntes and why it's necessary ?

33) What is CRD's in kubernetes and what's the advantage of it ?

34) What are labels and selectors in kubernetes ?

35) How pods in kubernetes will talk to each other ( How inter-service-communication between the pods work ? )

36) What is service discovery mechanism in kubernetes? 

37) What are the types of Services Available In Kubernetes ?

38) What is Cluster IP, Load Balancer Serive and Node Port Service and when when to what ?

39) What is External Name Service In Kubernetes and what's the advantage of it ?

40) Which service do we use when you want to expose any service outSide the kubernetes cluster ?

41) You'd like to expose 15 services in your kubernets cluster ? Do you use 15 Load Balancer Serices ? How would you solve this keeping cost in mind ?

42) What is an Ingress Controller In K8's ?

43) What is Ingress vs Ingress Controller ?

44) What are the Popular Ingress Controller Products ? Nginx Ingress Controller , HA Proxy Ingress Controller, Istio

45) Using Ingress, how can we create the Load Balancer Service with NETWORK Load Balancer on AWS ?

46) How can we define whether the Load Balancer Provisioned on the cluster as Network or Application Load Balancer ?

47) What is an annotation in kubernetes ? What's the different between annotation and labels ?

48) Are Kubernetes annotations specific to cloud provider ?

49) Do we have any character limiations on labels and selectors ?

50) What is a set in kubernetes ?

51) Replica Set vs Deployment Set vs Statement Set vs Deployment Set ?

52) I want to deploy a minimum of one pod in each and every node of my kubernetes cluster and that should be coming up automatically on the new nodes that comes up as apart of the auto-scaling, how can we handle this and what type of set do you use ?

53) What's the major different between Deployment Set vs Replica Set ?

54) What is the Default Deployment Strategy in Deployment ?

55) Rolling Update vs Recrete Strategy In Kubernetes ?

56) How to control the % of pods that are going to update in a deployment as apart of the Rolling Update ? 

57) Max Surge vs Max Available in Kubernetes Cluster as apart of the Cluster Update ?

58) My kubernetes cluster version 1.24.2, can I directly update to 1.26.0 ? No, one minor versio at a time !!!!

59) What is the stateful vs Stateless Applicaiton ?

60) Can we create Databases or Applications that need Storage or Persistent Volume in Kubernetes ?

61) What is Persistent Volume vs Persistent Volume Claim or PV vs PVS in Kubernetes ?

62) What is Storage Class In Kubernetes and what's the use of it ?

63) We have 3 customer work loads in our Kubernetes Cluster and we would like provision Persistent Volumes of type SSD to Cusomter-A ( Permium Customer) and for rest of the customer we would like to provison PV's of type HDD, how can we deal that ?

64) What is Pod Priority and Preemption in Kubernertes ?
    
    ```
        https://kubernetes.io/docs/concepts/scheduling-eviction/pod-priority-preemption/
    ```

65) How pods of a deployment know that it has to go and attach to the specific deployment set only ?

66) Will deployment set will has an IP Address ?

67) How requests of a service will go a pods ? How reqeusts to a service know that it has to go a pods of a set ?

68) Why Labels and Selectors are key attribute in Kubernetes ?

69) What are Taints and Tolerations On Kubernetes ?

70) What is a Node Selector In Kubernetes ?

71) How can we label the nodes of a node-pool ?

72) How can we target that POD's a deployment will run a specific node or specific set of nodes ?

    ```
        Label the nodes and then on the deployment manifest use nodeSelector and this makes the pod to run on that node / nodePool
    ```

73) Can we run pods on Nodes that are tainted ?

74) How can I run the pods on a node tha are TAINED ? Use the appropriate tolerations on the deployment!

    ```
        https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/
    ```
75) How to taint a node ?

```
       $ kubectl taint nodes node1 key1=value1:NoSchedule
       $ kubectl taint nodes node1 key2=value2:NoExecute

```

76) What is Pod Overhead ?

78) What are probes and why we need them ?

79) Liveliness Probes vs Readiness Probes vs Start up probes in kubernetes ?

80) What is Resource Quota in K8's ? What are limits and requests and why we would be using it ?

81) Can we limit the maximum CPU or Memory consumed by workloads in total at nameSpace level ?

82) What is Node-pressure Eviction ?

```
    Node-pressure eviction is the process by which the kubelet proactively terminates pods to reclaim resources on nodes.

    The kubelet monitors resources like memory, disk space, and filesystem inodes on your cluster's nodes. When one or more of these resources reach specific consumption levels, the kubelet can proactively fail one or more pods on the node to reclaim resources and prevent starvation.

    During a node-pressure eviction, the kubelet sets the phase for the selected pods to Failed, and terminates the Pod.
```

83) What is Pod Security Admission ?

84) What is a Pod Disruption Budget and how it plays an important role in achieving Fault Tolerance ?

85) What is admission control in kubernetes ?

86) Can Pods in default nameSpace communicate with pods in another nameSpace ? If yes, what' the service name or FQDN Of the Service To Be Used ?

87) What is Network Policy, Ingress and Egress and Kubernetes ?

88) How can we disable communication between the Pods in nameSpace-A and nameSpace-B

89) What is the user of Stateful Sets and under what situations do we use them ?

90) How scale up and down happens in Stateful Set, do they follow any order of scale up and down ?

91) What is a headLess service in kubernetes ?

92) Can we run more than one container in a Kubernetes pod ?

93) Will each and every container in the pod will have an IP Address ?

94) Why do we use multi-container pods ?

95) Will multi-container pods share the network and storage ?

96) What is a Side Car Container in Kubernetes ?

97) What are the famous sideCar patterns in Kubernets ?

```
    https://kubernetes.io/blog/2023/08/25/native-sidecar-containers/
```

98) What is a INIT Container In Kubernetes Deployments and why do we use it ?

99) What is JOB in Kubernetes and why do we use it ?

100) How do you stream the logs of a specific container is a Multi-Cotainer Pod ?

101) What is a Shell Less or Distroless container in Kubernetes ?

102) If your POD doesn't have a shell, how can we enter in to it or see the environment variables of the pod ?

103) ConfigMap vs Secret In Kubernetes ?

104) If we update the values of a ConfigMap, will the pods that have already using it will get the updated values ?

105) What are the disadvantages of Secrets In Kubernetes ?

106) What is an event in Kubernets ? How can we see the events in your cluster or a specific nameSpace ?

107) What are the various stages of a pod that you've seen ?

108) What all could be the reasons for pod been staying in pending state ?

109) How can we increase the persistent volume that was assigned to a specific deployment ?

110) How do list the available API Versions in K8's ?

111) What is Kubelet and what's teh use of it ? And why each and every node needs to have a kubelet ?

112) How to scale the pods from 3 to 8 of a deployment ?

113) What is ROLE vs Cluster Role in Kubernetes ?

114) What are static pods in a kubernertes cluster and why we would be needing that ?

115) How can we dry-run a pod ?

116) How your Kubernetes deployments can pull the container images from ECR or GCR ? How authentication between EKS to ECR happen ?

117) How to do maintenance activity on the K8 node ?

118) How can you evict the resources running on a specific kubernetes node before you start maintenance on it ?

```
    $    kubectl drain <node_name> –ignore-daemonsets

```

119) How can we mark the node not to accept or schedule workloads on it ?

```
    $      kubectl cordon <node_name>
```

120) What is cordoning a node and how to do that ?

121) What are the various things that can be done to increase security in Kubernetes ?

```
    a. Usage of RBAC (Role-Based Access Control)
    b. Pod Security Policies
    c. Ensure Network Policies are in place 
    d. Implement Pod Security Context
    e. Secure Secrets Management
```


122) What is KubeProxy and KubeDNS in Kubernetes and what's the role of it ?

123) What is a Federated Cluster ?
```
    Multiple Kubernetes clusters can be managed as a single cluster with the help of federated clusters. So, you can create multiple Kubernetes clusters within a data center/cloud and use federation to control/manage them all at one place.
```



124) List some of the types of Kubernetes volumes.

```
    EmptyDir: This volume is first created when a node is assigned with a pod. Initially, it is empty. A volume of type emptyDir is available for the lifetime of the pod.

    Flocker: It is an open-source and clustered container data volume manager.

    HostPath: This volume mounts a file or directory from the host node's filesystem into the pod. It can provide access to host files or share files between containers on the same host.

    NFS: Network File System (NFS) allows computers to either access or share files over the network. It is a dedicated file storage when multiple users must retrieve data for centralized disk capacity.
```

125) How to safely drain a node when you wish to start maintenance on it ?

126) How to schedule pods on a node that's tainted ?

127) What is a Shell-Less Pod ?

128) How can we prevent running the containers of a pod as a root user ?

129) What is a sidecar and when is it best to use one?

130) How do you implement service discovery internally in a Kubernetes cluster?

131) What is the different between a pod and job in kubernetes and why the status of a Job shows as completed ?

132) If a pod exceeds its memory "limit" what signal is sent to the process?

133) What is Port-forwarding and what's the use of it in Kubernetes ?

134) What are the different types of multiple-container pods?

```
There are three different types of multi-container pods. They are as follows:

    Sidecar: The Sidecar pattern is a single node pattern made of two containers of the application. It contains the core logic of the application and it sends the logic files to the bucket.

    Adapter: It is used to standardize and normalize the output application or monitor data for aggregation. It performs restructuring, and reformatting and can write the correct formatted output for the application.

    Ambassador: It is a proxy pattern that allows connecting other containers with a port on the localhost.

```

135) What is North-South, East-West Communicaiton In Kubernetes ?

136) What's the easiest way to enable TLS between 2 services in K8's ?

137) Is it recommended to enable TLS between the services in Kubernetes ?

138) What is Garbage Collection in Kubernetes and what's the purpose of it ?

```
Garbage collection is a collective term for the various mechanisms Kubernetes uses to clean up cluster resources. This allows the clean up of resources like the following:

    a. Terminated pods
    b. Completed Jobs
    c. Objects without owner references
    d. Unused containers and container images
    e. Dynamically provisioned PersistentVolumes with a StorageClass reclaim policy of Delete
    f. Stale or expired CertificateSigningRequests (CSRs)
    g. Nodes deleted in the following scenarios:
    h. On a cloud when the cluster uses a cloud controller manager
    i. On-premises when the cluster uses an addon similar to a cloud controller manager
```



139) What is Pod Disruption

```
    Pod disruption is the process by which Pods on Nodes are terminated either voluntarily or involuntarily.

    Voluntary disruptions are started intentionally by application owners or cluster administrators. Involuntary disruptions are unintentional and can be triggered by unavoidable issues like Nodes running out of resources, or by accidental deletions.

    And it could be of any of the below reasons :

        * Pod Priority and Preemption
        * Node-pressure Eviction
        * API-initiated Eviction

```

140 ) What is Node Pressure Eviction vs API-Initiated Eviction ?

```
    Node-pressure eviction is the process by which the kubelet proactively terminates pods to reclaim resources on nodes.

    The kubelet monitors resources like memory, disk space, and filesystem inodes on your cluster's nodes. When one or more of these resources reach specific consumption levels, the kubelet can proactively fail one or more pods on the node to reclaim resources and prevent starvation.

    During a node-pressure eviction, the kubelet sets the phase for the selected pods to Failed, and terminates the Pod.

    Node-pressure eviction is not the same as API-initiated eviction.

    The kubelet does not respect your configured PodDisruptionBudget or the pod's terminationGracePeriodSeconds. If you use soft eviction thresholds, the kubelet respects your configured eviction-max-pod-grace-period. If you use hard eviction thresholds, the kubelet uses a 0s grace period (immediate shutdown) for termination.


```

141) What is API-initiated Eviction ? 

```

    API-initiated eviction is the process by which you use the Eviction API to create an Eviction object that triggers graceful pod termination.

    You can request eviction by calling the Eviction API directly, or programmatically using a client of the API server, like the kubectl drain command. This creates an Eviction object, which causes the API server to terminate the Pod.

    API-initiated evictions respect your configured PodDisruptionBudgets and terminationGracePeriodSeconds.

    Using the API to create an Eviction object for a Pod is like performing a policy-controlled DELETE operation on the Pod.

```

142) What is a Cron Job In Kuberetes ?

```
    CronJob is meant for performing regular scheduled actions such as backups, report generation, and so on. One CronJob object is like one line of a crontab (cron table) file on a Unix system. It runs a Job periodically on a given schedule, written in Cron format.
```


143) What is a Pod Overhead ?

```
    FEATURE STATE: Kubernetes v1.24 [stable]
    
        When you run a Pod on a Node, the Pod itself takes an amount of system resources. These resources are additional to the resources needed to run the container(s) inside the Pod. In Kubernetes, Pod Overhead is a way to account for the resources consumed by the Pod infrastructure on top of the container requests & limits.

    In Kubernetes, the Pod's overhead is set at admission time according to the overhead associated with the Pod's RuntimeClass.

    A pod's overhead is considered in addition to the sum of container resource requests when scheduling a Pod. Similarly, the kubelet will include the Pod overhead when sizing the Pod cgroup, and when carrying out Pod eviction ranking.

```