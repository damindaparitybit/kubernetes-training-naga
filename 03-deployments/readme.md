Create Pod
```kubectl run nginx --image nginx --restart Never --port 80 --dry-run -o yaml > pod-nginx.yaml```

Create Deployment
```kubectl run nginx --image nginx --restart Always --port 80 --dry-run -o yaml > deployment-nginx.yaml```

 ```kubectl apply -f deployment-nginx.yaml```

 Force delete a pod
 ```kubectl delete pod <pod-name> --force --grace-period=0```

 Deploymnet commands
 ```kubectl get deployments```

 First step of debugging
 ```kubectl describe deplyment```

 Edit on the fly
 ```kubectl edit deploy nginx```

 Export the yaml
 ```kubectl get deploy nginx --export -o yaml > deployment-nginx.yaml```

Get Replicasets
```kubectl get rs```

Get Deployment History
```kubectl rollout history deploy/nginx```

Rollback
```kubectl rollout undo deploy/nginx --to-revision 2```

Pause Update
```kubectl rollout pause deploy/nginx```

Delete all pods in a namespace
```kubectl delete pods --all ```

Create a pod and exec
```kubectl run -it busybox --image busybox:1.27 --restart Never --rm -- /bin/sh```
