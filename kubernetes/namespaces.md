# Namespaces

Allow to group resources.e.g. Dev, Test, Prod 

K8s creates a defaultnamespace called **default**

Objects in one namespace can access objects in a different namespace
- e.g. objectname.prod.svc.cluster.local

Deleting a namespace will delete all its child objects

## Define a namespace
```
apiversion: v1
kind: Namespace
metadata:
  name: prod
```
## Specify the namespace while defining objects
```
apiversion: v1
kind: Pod
metadata:
  name: myapp prod
  namespace: prod
spec:
  containers:
    name: nginx container
    image: nginx
```

## kubektcl - Namespace cheat sheet
- ```kubectl get namespace``` List all namespaces
- ```kubektcl get ns``` Shirtcut to get all namespaces
- ```kubectl config set-context --current --namespace=<namespaceName>``` Set the current context to use a namespace
- ```kubektcl create ns <namespaceName>``` Create a namespace
- ```kubektcl delete ns <namespaceName>``` Delete a namespace
- ```kubektcl get pods --all-namespaces``` List all pods in all namespaces
