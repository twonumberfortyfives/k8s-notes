![[Excalidraw/pods|pods]]
## Pod creation flow

1. The Kubernetes scheduler tells a Node to run a Pod.
2. On that Node, the kubelet receives the request from Kubernetes.
3. Kubelet calls the CNI plugin to setup nerworking for that Pod.
4. The CNI plugin:
	- Creates a network interface for the Pod.
	- Connects it to the Node virtual overlay network.
	- Assigns an IP Address to the Pod from the CNI managed subnet.
5. Kubelet then starts the Pod's containers, telling them:
	- Here is your network namespace (shared among all containers in the Pod).
	- Here is your IP Address from CNI