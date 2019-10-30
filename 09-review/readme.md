Part I

Run a deployment of docker image nextcloud. https://hub.docker.com/_/nextcloud/
nextcloud container runs on port 80

PVC - PersistentVolumeClaims
Create 2 PVCs for 1GB using GCP Persistent Disks (class=standard) and name them html and mysql
Mount the 2 PVCs to the nextcloud pod on the paths /var/www/html and /var/lib/mysql

Make sure the deployment only has 1 replica

expose the deployment as a service of type loadbalancer

Save up all the yamls

Part II

create a deployment named platformer-demo using the image nilesh93/pxe-demo:latest
container runs on port 8080

expose the deployment as a service loadbalancer.

create a configmap using the file config.json 
Mount the configmap FILE ONLY into the container on the mount path /app/config/config.json

save up all the yamls


Part III

kubectl apply -f bad-busybox.yaml

This pod will go into a crashloop.
get the log output of the pod for a error.txt file and find a way to fix the pod
hint: empty dir and init containers