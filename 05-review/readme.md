Part I 

Create a namespace called ghost

Create a deployment for the application ghost inside the namespace ghost
https://hub.docker.com/_/ghost/
The container port is 2368

Expose the deployment as a service type loadbalancer in which service port should be 80 and be inside the namespace ghost

Save up all the yamls

Solution:

```kubectl create ns ghost```
```kubectl run ghost --image ghost -n ghost --port 2368 --restart Always --dry-run -o yaml > deployment-ghost.yaml```
```kubectl expose deploy/ghost --port 80 --target-port 2368 --type LoadBalancer --dry-run -o yaml > service-ghost.yaml```

Part II

Get the logs of the ghost pod into a text file called ghost-logs.txt

kubectl logs ghost-797ffd5766-jmsgl -n ghost >ghost-logs.txt


Run busybox:1.27 image and get the output of nslookup for the dns resolution of ghost service and the ghost pod into 2 files named ghost-pod-dns.txt and ghost-svc-dns.txt
kubectl run -it busybox --image busybox:1.27 -n ghost --restart Never --rm -- /bin/sh
kubectl run -it busybox --image busybox:1.27 -n ghost --restart Never --rm -- nslookup 10-8-0-3.ghost.pod > ghost-pod-dns.txt
kubectl run -it busybox --image busybox:1.27 -n ghost --restart Never --rm -- nslookup ghost.ghost.svc >ghost-svc-dns.txt
