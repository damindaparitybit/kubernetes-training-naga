kubectl run nginx --image nginx --port 80 --restart Never -n naga
kubectl get pods -n naga
kubectl get pods -n naga --show-labels
kubectl get pods -n naga -l run=nginx
kubectl get pods -n naga -o wide
kubectl describe pod nginx -n naga
kubectl port-forward po/nginx 3000:80 -n naga
kubectl exec -it nginx -n naga  -- /bin/sh
kubectl logs nginx -n naga
kubectl run nginx --image nginx --port 80 --restart Never -n naga --dry-run -o yaml > pod-nginx.yaml
kubectl explain Pod.spec
kubectl apply -f pod-nginx.yaml -n naga 
kubectl delete pod -n naga nginx
kubectl run nginx --image nginx --port 80 --restart Never -n naga --dry-run -o json > pod-nginx.json