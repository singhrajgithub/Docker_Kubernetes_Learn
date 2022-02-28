# Learn Kubernetes

Kubernetes Uses :
1) Container Orchestration --> Manage 1000s containers instances.
2) Features --> Auto Scaling, Service Discovery , Load Balancing , Self healing , Zero Downtime Deployments.
3) Cloud Neutral --> Standardized Platform on any Infrastructure.



![Kubernetes_Use](https://user-images.githubusercontent.com/24280813/156001340-df9795ac-ae40-4381-b379-35e25ac6cf76.JPG)


# Kubernetes Architecture 

At very high level Kubernetes has below architecture :

![highLevel_KubernetesArchitecture](https://user-images.githubusercontent.com/24280813/156025630-dbf896f1-3c7c-42d9-9ed4-25a267aff4a3.JPG)

# Connect with Kubernetes Cluster via gcloud

1) gcloud container clusters get-credentials [cluster-name] --zone [selected zone name] --project [project-name]
2) After connecting to the cluster we need to use kubectl to interact with the cluster.
3) kubectl is be default installed on cloudshell
4) kubectl create deployment hello-world-rest-api --image=hello-world-rest-api:0.0.0.1.RELEASE   -->[ create new deploymentin kubernetes.]
5) kubectl expose deployment hello-world-rest-api --type=Loadbalancer --port=8080
6) kubectl scale deployment hello-world-rest-api --replicas=3
7) kubectl delete pod hello-world-rest-api-58ff5dd898-62l9d
8) kubectl autoscale deployment hello-world-rest-api --max=10 --cpu-percent=70
9) kubectl edit deployment hello-world-rest-api #minReadySeconds: 15
10) kubectl set image deployment hello-world-rest-api hello-world-rest-api= hello-world-rest-api:0.0.2.RELEASE
11) gcloud container clusters get-credentials cluster --zone us-central1-a --project solid-course-258105
12) kubectl create deployment hello-world-rest-api --image= hello-world-rest-api:0.0.1.RELEASE
13) kubectl expose deployment hello-world-rest-api --type=LoadBalancer --port=8080
14) kubectl set image deployment hello-world-rest-api hello-world-rest-api=DUMMY_IMAGE:TEST
15) kubectl get events --sort-by=.metadata.creationTimestamp
16) kubectl set image deployment hello-world-rest-api hello-world-rest-api= hello-world-rest-api:0.0.2.RELEASE
17) kubectl get events --sort-by=.metadata.creationTimestamp
18) kubectl get componentstatuses
19) kubectl get pods --all-namespaces
20) kubectl get events
21) kubectl get pods
22) kubectl get replicaset
23) kubectl get deployment
24) kubectl get service
25) kubectl get pods -o wide
26) kubectl explain pods
27) kubectl get pods -o wide
28) kubectl describe pod hello-world-rest-api-58ff5dd898-9trh2
29) kubectl get replicasets
30) kubectl get replicaset
31) kubectl scale deployment hello-world-rest-api --replicas=3
32) kubectl get pods
33) kubectl get replicaset
34) kubectl get events
35) kubectl get events --sort.by=.metadata.creationTimestamp
36) kubectl get rs
37) kubectl get rs -o wide
38) kubectl set image deployment hello-world-rest-api hello-world-rest-api=DUMMY_IMAGE:TEST
39) kubectl get rs -o wide
40) kubectl get pods
41) kubectl describe pod hello-world-rest-api-85995ddd5c-msjsm
42) kubectl get events --sort-by=.metadata.creationTimestamp
43) kubectl set image deployment hello-world-rest-api hello-world-rest-api= hello-world-rest-api:0.0.2.RELEASE
44) kubectl get events --sort-by=.metadata.creationTimestamp
45) kubectl get pods -o wide
46) kubectl delete pod hello-world-rest-api-67c79fd44f-n6c7l
47) kubectl get pods -o wide
48) kubectl delete pod hello-world-rest-api-67c79fd44f-8bhdt
49) kubectl get componentstatuses
50) kubectl get pods --all-namespaces
51) gcloud auth login
52) kubectl version
53) gcloud container clusters get-credentials cluster --zone us-central1-a --project solid-course-258105
54) kubectl rollout history deployment hello-world-rest-api
55) kubectl set image deployment hello-world-rest-api hello-world-rest-api= hello-world-rest-api:0.0.3.RELEASE --record=true
56) kubectl rollout undo deployment hello-world-rest-api --to-revision=1
57) kubectl logs hello-world-rest-api-58ff5dd898-6ctr2
58) kubectl logs -f hello-world-rest-api-58ff5dd898-6ctr2
59) kubectl get deployment hello-world-rest-api -o yaml
60) kubectl get deployment hello-world-rest-api -o yaml > deployment.yaml
61) kubectl get service hello-world-rest-api -o yaml > service.yaml
62) kubectl apply -f deployment.yaml
63) kubectl get all -o wide
64) kubectl delete all -l app=hello-world-rest-api
65) kubectl get svc --watch
66) kubectl diff -f deployment.yaml
67) kubectl delete deployment hello-world-rest-api
68) kubectl get all -o wide
69) kubectl delete replicaset.apps/hello-world-rest-api-797dd4b5dc
70) kubectl get pods --all-namespaces
71) kubectl get pods --all-namespaces -l app=hello-world-rest-api
72) kubectl get services --all-namespaces
73) kubectl get services --all-namespaces --sort-by=.spec.type
74) kubectl get services --all-namespaces --sort-by=.metadata.name
75) kubectl cluster-info
76) kubectl cluster-info dump
77) kubectl top node
78) kubectl top pod
79) kubectl get services
80) kubectl get svc
81) kubectl get ev
82) kubectl get rs
83) kubectl get ns
84) kubectl get nodes
85) kubectl get no
86) kubectl get pods
87) kubectl get pod
88) kubectl delete all -l app=hello-world-rest-api
89) kubectl get all
90) kubectl apply -f deployment.yaml 
91) kubectl apply -f ../currency-conversion/deployment.yaml
