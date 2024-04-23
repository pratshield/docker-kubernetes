## Pod state
- **Pending**
  - Accepted but not yet created
- **Running**
  - Bound to a node
- **Succeeded**
  - Exited with status 0
- **Failed**
  - All containers exited with atleast one of the container exit with non zero exit code
- **Unknown**
  - Communication issues with the pod
- **CRashLoopBackOff**
  - Started, Crashed, Started again and Crashed again
 
## Define Pod

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
    ports:
    - containerPort: 80
      name: http
      protocol: TCP
    env:
    - name: DBCON
      value: connectionstring
    command: ["bin/sh", "-c"]
    args: [echo ${DBCON}]
```
