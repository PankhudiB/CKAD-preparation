So the problem statement said :

`Create a Service named redis-service of type ClusterIP to expose pod redis on port 6379`

 -> what i missed - and later understood is - that the intent is to be able to expose the pod's port via svc

-> lets say i use commands to do that, but then how to do I figure if the port exposing is succcesful 

-> To verify 
Exec into the pod and do `netstat` -> gives precise feedback.

