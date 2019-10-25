Create a pod
```kubectl run busybox --image busybox --restart Never -o yaml --dry-run > pod-busybox.yaml```
```kubectl delete pod busybox --force --grace-period=0```

SSH and run env command on the main terminal
```kubectl exec -it busybox -- env```

Create a config map
```kubectl create cm literal-example --from-literal country=US --from-literal gender=male --dry-run -o yaml > cm-from-literal.yaml```

Get configmaps
```kubectl get cm```

Create configmap from File
``` kubectl create cm from-file --from-file config.properties --dry-run -o yaml > cm-from-file.yaml```