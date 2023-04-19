#Core Concepts

### Node:

1. Cluster - set of node
2. Master - actual orchestration onf containers running on worker Node
3. Components
    1. API server - frontend - cli
    2. Scheduler - looks for new containers - and assigns them to node
    3. kubelet - agent that runs on each node - to make sure containers are running as expected
    4. container runtime - underlying s/w to run container - docker
    5. controller - brain behind orchestration ,
    6. etcd - distributed KV store

4. kubectl run command - to deploy application in the cluster
5. kubectl cluster-info
6. kubectl get-nodes
============
7. u can install containerD independently.

### Pod:
1. containers encapsulated inside Pod 
2. smallest obj in k8s

```yaml

apiVersion: v1  <--- for POD
kind: Pod 
metadata: <--- DICTIONARY --> allowed name and labels key
name: myapp-pod
labels: <---------- DICTIONARY under labels - any key-value 
      app: front-end <---- can be used to group multiple pods
spec: <-------- different for different object
containers: <- LIST ----- since Pod can have multiple containers
      - name: nginx-container
        image: nginx 

```

```yaml
apiVersion: v1
kind: Pod
metadata:
   name: myapp-pod
   labels:
      app: myapp
spec:
```

Lab exercises that were new to me other than usual stuff: 

1. get all names of the container running in given pod
   ```kubectl get pods POD_NAME -o jsonpath={.spec.containers[*].name}```

2.  To create a pod with redis image - without yaml file: 
   ```kubectl run nginx-container --image=nginx```
3. 


