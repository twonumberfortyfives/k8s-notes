![[volumes]]

Persistent volume can be explained as cluster resource like CPU or RAM but for storing data. (Abstract component)
- Created by yaml file
- Persistent volume is just an interface to your real storage or physical local storage (on the node itself)
- Are not namespaced (available to the whole cluster) 

### Persistent volume claim
![[persistent-volume-claim]]
You can make Persistent Volume available to all pod's containers
You can also make PV available to specific container via defining containers yaml Pod config
AND when a pod dies the new created pod will use the same pv claim to get access to pv

### Storage class
![[]]