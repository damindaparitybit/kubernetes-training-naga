 kubectl run emptydir-busybox --image busybox --restart Always --dry-run -o yaml > emptydir-busybox-deploy.yaml


  kubectl run hostpath-busybox --image busybox --restart Always --dry-run -o yaml > hostpath-busybox-deploy.yaml