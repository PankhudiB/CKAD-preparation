## NAMESPACES

1. same old - isolation and separation within the cluster
2. As long as yaml file is concerned:
   1. ns-definition.yml
   ```
   apiVersion : v1
   kind : Namespace
   metadata: 
      name: dev
   ```   
   
   2. key can be used under metadata of Pod-definition.yml

   ```
   metadata:
      name: my-pod
      namespace: blah 
   ```
   
3. To set by default ns for working

``` kubectl config set-context $(kubectl config current-context) --namespace=dev```

