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


Check if your Persistent Volume Claim is bound or not?
```
kubectl get po,statefulsets,deploy,svc,pvc


[output]
NAME                           READY     STATUS    RESTARTS   AGE
po/frontend-55c8f59bd8-2vrqf   1/1       Running   0          46m
po/frontend-55c8f59bd8-prk5z   1/1       Running   0          46m
po/nfs-provisioner-0           1/1       Running   0          55m

NAME                           DESIRED   CURRENT   AGE
statefulsets/nfs-provisioner   1         1         55m

NAME              DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
deploy/frontend   2         2         2            2           46m

NAME                  TYPE        CLUSTER-IP       EXTERNAL-IP       PORT(S)                              AGE
svc/frontend          NodePort    10.107.221.245   128.199.167.209   8079:32694/TCP                       46m
svc/nfs-provisioner   ClusterIP   10.110.60.106    <none>            2049/TCP,20048/TCP,111/TCP,111/UDP   55m

NAME      STATUS    VOLUME                                     CAPACITY   ACCESS MODES   STORAGECLASS   AGE
pvc/nfs   Bound     pvc-d6dc3908-1d37-11e8-ab45-02ab3bf0d4f7   1Mi        RWX            example-nfs    54m
```

If everything is working fine, your output shold look like what is given above (mainly pvc should have a **Bound** status). 

You need to know the following, 
  - Managing pods
  - Statefulsets
  - RBAC 
     - Service Accounts 
     - Cluster Roles and Roles 
     - Cluster Role Bindings 
  - Namespaces
  - Persistent Volumes 
     - Storage Classes
     - PV and PVC 



