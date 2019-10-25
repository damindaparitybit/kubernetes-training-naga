Create a namespace called review2
Inside the namespace, create a configmap with key value pairs of name=naga, country=us and also have the file mysql.properties on the SAME FILE.

Create a busybox deployment that would be running for 3600 seconds by editing command.
inject the env variable name from the configmap and make sure the linux env variable is renamed to NAME
mount the rest of the configmap using envFrom.

All of these in the namespace review2