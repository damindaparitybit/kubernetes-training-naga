
Part I - Deployments

Create a deployment for Nextcloud https://hub.docker.com/_/nextcloud 
container runs on port 80
Create 2 PVCs for 1GB using GCP Persistent Disks and name them html and db
Mount the 2 PVCs to the pods on the paths /var/www/html and /var/lib/mysql

Make sure the deployment only has 1 replica

expose the deployment as a service of type loadbalancer

Save up all the yamls


Part II - Scaling up the Deployment

Scale up the nextcloud deployment for 3 replicas.
Does they start up? what is the status of the pods?
Any reason for that state?


Part III - Statefulset

Create a statefulset from the information from Part I.
Note, you don't have to create PVCs this time, you can use pvc template in statefulset spec
scale it up tp 3 replicas and observe the difference.