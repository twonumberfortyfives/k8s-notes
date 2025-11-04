All pods have their own IP addresses. The problem is that pods are ephemeral - are destroyed frequently (After restart, or destory IP address is changing). Service solves this issue by creating or defining stable IP address.
![[Pasted image 20251104103035.png]]
![[Pasted image 20251104103308.png]]
![[Pasted image 20251104103604.png]]
### Cluster IP Services
![[services]]
By default whenever you create service it will be Cluster IP Service. Receives internal requests and reroutes them to clarified pod in Service yaml selector in selector what references to pod's labels.
Can be also defined target ports (IS ONLY ACCESSIBLE WITHIN A CLUSTER)
### NodePort Services
![[nodeport-service]]
EXTERNAL TRAFFIC HAS ACCESS TO FIXED PORT ON EACH WORKER NODE
Creates Cluster IP Automatically


### Headless Services
![[headless-service]]
In this case you want you NodePort if you want to have communications between pods directly and specifically, not randomly selected. And this time it's about Stateful applications like databases where pods replicas are unique and not identical (master pod and worker replicas). 

it’s used for **direct pod-to-pod communication** _inside your application_ — when you **don’t want load balancing** and **do want each pod’s IP** to be discoverable.

### LoadBalancer Services
![[loadbalancer-service]]
Creates Cluster IP, NodePort  Automatically. LoadBalancer itself provided by cloud provider.