
`difficulty: easy`

### STEPS

  * Apply deployments and service

```
kubectl apply -f frontend-deploy.yml
kubectl apply -f frontend-svc.yml
```
  * Try to access the service using nodeport 

```
kubectl get svc

[output]
NAME              TYPE        CLUSTER-IP       EXTERNAL-IP       PORT(S)                              AGE
frontend          NodePort    10.107.221.245   128.199.167.209   8079:32694/TCP                       17s
```

```
curl <HOSTIP:<NODEPORT>>
```

`Problem : even though pods and deployments are running, service is created, application does not load.`

Fix it ! 

Skills Needed: 
  - Pods 
  - Services
  - Deployments
