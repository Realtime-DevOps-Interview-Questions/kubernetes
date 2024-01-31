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

