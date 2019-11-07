```kubectl create secret generic sample-secret --from-literal foo=bar --from-literal name=naga -o yaml --dry-run > literal-secret.yaml```

```kubectl create cm  sample-secret --from-literal foo=bar --from-literal name=naga -o yaml --dry-run > literal-cm.yaml ```

```kubectl get secrets```
```kubectl get secret sample-secret -o yaml --export```


 kubectl run busybox --image busybox -o yaml --dry-run > busybox.yaml


 deploy.spec.template ======== pod;

 If you want the contents of pod.spec.containers ---> deploy.spec.template.spec.containers