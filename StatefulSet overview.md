![[statefulset]]

So there is two type of applications in k8s
- Stateful
- Stateless

### Stateful application
1. Are applications what store data like databases;
2. Replecating apps is more difficult;
3. Can't be created or deleted in the same time;
4. Can't be randomly addressed;
5. Replica Pods are not identical;
6. Has sticky identity for each pod;
7. Only ONE pod is allowed write / change data;
8. Master pod is defined and chosen, others are workers;
9. Replicas are not using the same physical storage;
10. Continuous syncronization all replicas storages are trying to keep consistency and clone data from prev. replica pod
11. When you create replicas will be created step by step only after master pod is up and running
12. When you delete replicas it will start deleteing pods from the end

### Stateless application
1. Do not keep states of records; 
2. Each request / interaction completely handled as new isolated interaction;