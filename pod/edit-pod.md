
### Editing the pod

1. If you are given a pod definition file, edit that file and use it to create a new pod using `vi`


2. If you are not given a pod definition file, you may extract the definition to a file using the below command:

    `kubectl get pod <pod-name> -o yaml > pod-definition.yaml`
    
    Then edit the file to make the necessary changes, delete and re-create the pod.
   

3. Use the `kubectl edit pod <pod-name>` command to edit pod properties.

