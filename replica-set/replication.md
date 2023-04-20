
#replication-controller

1. helps in High availability 
2. helps us run multiple instances of the same pod
3. load balancing and scaling


REPLICATION CONTROLLER VS REPLICA SET

both have same purpose - but the same
REPLICATION CONTROLLER - is being replaced by - REPLICA SET

Logically 
replica set is on top of a pod

so while writing the replica-set.yml

1. kind: ReplicaSet
2. spec:
   3. template: 
      4. whose ??? - we will have to pass pod template except kind and apiVersion key-value
      
   4. replicas : NO_OF_REPLICAS 
   5. selector: <--- major differentiator than replication controller
      1. Replica set - uses selector 
         1. now why to use this again if you have already specified pod template above ?
         2. To also maintain replicas of pod that were not created through this replica set 
          but still annotated under the tag
   
      
