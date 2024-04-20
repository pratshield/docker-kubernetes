# K8s Context
- A context is a group of access parameters to a K8s cluster
- Context contains a Kubernetes cluster, a user, and a namespace
- The current context is the cluster that is currently set a s default for kubectl and all kubectl commands run against that default cluster

## kubectl - context cheat sheet
- ```kubectl config current-conext``` Get current context
- ```kubectl config get-contexts``` List all context
- ```kubectl config use-context <contextName>``` Set the current context
- ```kubectl config delete-context <contextName>``` Delete acontext from config file

## Kubectx - quickly switch context
Instead of typing:

```kubectl config user-context <contextName>```

simply type:

```kubectx <contextName>```
