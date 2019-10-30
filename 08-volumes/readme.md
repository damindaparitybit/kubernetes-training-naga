 ## emptyDir
kubectl run emptydir-busybox --image busybox --restart Always --dry-run -o yaml > emptydir-busybox-deploy.yaml

## HostPath
kubectl run hostpath-busybox --image busybox --restart Always --dry-run -o yaml > hostpath-busybox-deploy.yaml

## Storage Class
 ```kuebctl get sc```


 ### command history

 4070  kubens naga
 4071  clear
 4072  kubectl get pv
 4073  clear
 4074  kubectl get pvc
 4075  cd 08-volumes
 4076  kubectl apply -f pvc-test.yaml
 4077  kubectl get pvc
 4078  kubectl get pv | grep pvc-385d2060-fb11-11e9-a6c1-42010a80011d
 4079  kubectl explain pod.spec.volumes
 4080  kubectl explain pod.spec.volumes.persistentVolumeClaim
 4081  clear
 4082  kubectl get cm
 4083  kubectl edit cm from-file 
 4084  kubectl explain pod.spec.volumes
 4085  kubectl explain pod.spec.volumes.configMap
 4086  kubectl get cm
 4087  kubectl apply -f cm-busybox-deploy.yaml
 4088  kubectl get pods
 4089  kubectl exec -it cm-busybox-6f4b6dfdc4-9gwhh  -- ls -ll /app
 4090  kubectl edit cm from-file
 4091  kubectl exec -it cm-busybox-6f4b6dfdc4-9gwhh  -- ls -ll /app
 4092  kubectl exec -it cm-busybox-6f4b6dfdc4-9gwhh  -- /bin/sh
 4093  kubectl explain pod.spec.containers.volumeMounts
 4094  clear
 4095  kubectl appy -f cm-busybox-deploy.yaml
 4096  kubectl apply -f cm-busybox-deploy.yaml
 4097  kubectl get pods
 4098  kubectl exec -it cm-busybox-67f846d596-54nlr  -- /bin/sh
 4099* cd ..
 4100* cd kubernetes-fundermentals-training
 4101* code .