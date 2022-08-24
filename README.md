
![](/kubernetes%20architecture%20explained.jpg)

## 1.Worker Nodes
* Each node contains multiple pods in it.
* 3 processes must be installed on every node: container runtime, kubelet,kubeproxy.
* **Container runtime** example- Docker.
* **Kubelet** interacts with both container and node. It starts the pod with a container
  inside.
* **Kubeproxy** forwards requests during commuication inside a node.

## 2.Master Nodes
* Managing processes like how to schedule a pod or monitor a pod are done by master nodes.
* 4 processes run on every master node: Api server, Scheduler, ControlManager and etcd
* **Api server** is a cluster gateway which gets updates or queries from the cluster.
  It acts as a guard for authentication.
* **Scheduler** schedules new pod. It decides the node to schedule a pod inside it.   
* **ControlManager** detects cluster state changes and perform necessary actions.
* **etcd**, known as the cluster brain, is a key-value store of a cluster state.
  Cluster state changes gets stored in the key-value store.


  
## How to add Master/Worker Nodes

* First get a bare new server.
* Install all the Master/Worker Node processes.
* Add it to the cluster.