# Init container

Initializes a pod before the application container runs

It useful to initiate some infrastructure code, dependency services like database, api etc that should be started before the application container runs.

> Init containers always run to completion

> Each init container must run successfully before the next init container starts

>If init container fails, kubelete restarts it untill it succeeds. May not restart depending on the restartPolicy, if set to Never.

## Define init containers

```
apiVersion: v1
kind: Pod
metadata:
  name: mykube-pod
  labels:
    app: mykube
    type: front-end
spec:
  containers:
  - name: nginx-container
    image: nginx
  initContainers:
  - name: init-myservice
    image: busybox:1.28
  - name: init-mydb
    image: postgresql
```
