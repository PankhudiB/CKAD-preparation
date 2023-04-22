

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
  labels:
    app: myapp
spec:
  containers:
    - name: nginx-container
      image: nginx
      ports:
        - containerPort: 8080 #<------ PORT
      command: ['','']        #<--- ENTRYPOINT of Dockerfile
      args: ['', '']          #<--- CMD of Dockerfile
      env:                    #<-------- LIST
        - name: some-name
          value: some-value   #<------ DIRECT VALUE
          valueFrom: 
              configMapKeyRef: #<------ VALUE FROM CONFIGMAP
          valueFrom: 
              secretKeyRef:   #<------ VALUE FROM SECRET
                
```