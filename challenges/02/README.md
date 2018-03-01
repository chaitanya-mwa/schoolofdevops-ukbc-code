# Challenge 02 - Persistent Volume

`Difficulty Level : Hard`

### STEPS

Create namespace and switch to it, 

```
kubectl apply -f  ns.yaml
kubectl config set-context $(kubectl config current-context) --namespace=challenge02
``` 

Create the following objects in that sequence, 

  * Service Account 

```
kubectl apply -f serviceaccount.yaml
```

  * Cluster Role 

```
kubectl apply -f clusterrole.yaml
```

  * Cluster Role Binding 

```
kubectl apply -f clusterrolebinding.yaml
```

  * Stateful Set 

```
kubectl apply -f statefulset-sa.yaml
```

  * Storage Class 

```
kubectl apply -f storageclass.yaml
```
  * PersistentVolumeClaim 

```
kubectl apply -f pvc.yaml
```

You are going to face issues while doing so. Make things work as you start creating these objects.. 

You need to know the following, 
  - Managing pods
  - Statefulsets
  - RBAC 
     - Service Accounts 
     - Cluster Roles and Roles 
     - Cluster Role Bindings 
  - Persistent Volumes 
     - Storage Classes
     - PV and PVC 



