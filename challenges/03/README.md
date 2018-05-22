# Challenge 02 - Persistent Volume

`Difficulty Level : Hard`

### STEPS


  * Service 

```
kubectl apply -f vote-03-svc.yaml
```
  * Deployment

```
kubectl apply -f vote-03-deploy.yaml
```

Once the deployment and service is created, find out the port that the service is been exposed and try to access it from the browser. 

  * Are you able to see the application when you load it from the browser
  * If not, why? 

Trace the issue and see if you could find the root cause. 



You need to know the following, 
  - Working with Services, NodePort
  - Creating, listing and describing deployments
  - Working with pods, Troubleshooting issues



