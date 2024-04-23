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

## kubectl pod cheat sheet

- ```kubectl create -f <pod-definition.yml>``` Create pod
- ```kubectl run <podName> --image=busybox -- bin/sh -c "sleep 3600"``` Run a pod
- ```kubectl get pods``` List all running pods 
- ```kubectl get pods -o wide``` List all running pods with more details
- ```kubectl describe pod <podName>``` Show pod info
- ```kubectl get pod <podName> -o yaml > file.yml``` Extract the pod definition from YAML file and save it to a file
- ```kubectl exec -it <podName> --sh``` Interactive mode
- ```kubectl delete -f <pod-definition.yml>``` Delete pod
- ```kubectl delete pod <podName>``` Delete the pod using podname
