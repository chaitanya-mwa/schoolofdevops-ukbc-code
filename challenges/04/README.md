
`Difficulty Level : Hard`

### STEPS


Apply the code 

```
kubectl apply -f  code/rethinkdb-quickstart.yaml
```

The above command should launch deployments and services for components related to rethinkdb. The following apps are launched, 
  * rethinkdb-replica
  * rethinkdb-admin
  * rethinkdb-proxy

Observe the deployments, pods and services.  

  * Do you see services and deployments for all three services listed above ? 
  * Do you see the pods running for each service/deployment ? 

Expected Observations: 

  * Services and Deployments are created 
  * Pods are not running for 2 out of 3 apps above   

Your goal is to trace the issue, find the root cause and fix it. 

Expected Outcome: 

  * All three services should be available with endpoints
  * All three deployments should have pods running and available 


Khowledge Prerequisite 

You need to know the following, 
  - Working with Pods, Deployments, Services 
  - Creating, listing and describing deployments
  - Working with pods, Troubleshooting issues
  - Ability to write RBAC Policies 
 



