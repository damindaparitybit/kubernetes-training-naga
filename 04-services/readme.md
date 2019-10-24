Create Deployment nginx
```kubectl run nginx --image nginx --restart Always --port 80 -o yaml > deployment-nginx.yaml```

Create a service for nginx deployment
```kubectl expose deploy/nginx --port 80 --target-port 80 --type ClusterIP -o yaml > service-nginx.yaml```

Get Services
``` kubectl get pods --show-labels```
```kubectl get svc```

Port forward the Service
```kubectl port-forward svc/nginx 3000:80```

Debug inside the cluster
```kubectl run -it busybox --image busybox:1.27 --restart Never --rm -- /bin/sh```

Service Discovery
```<service-name>.<namespace>.svc.cluster.local```
```nginx.naga.svc.cluster.local```

Pod DNS Discovery
```kubectl get pods -o wide```
```<pod-ip-with dashes>.<namespace>.pod.cluster.local```
```10-64-0-79.naga.pod.cluster.local```

Describe Service
```kubectl describe svc nginx```

Get Endpoints
```kubectl get ep```