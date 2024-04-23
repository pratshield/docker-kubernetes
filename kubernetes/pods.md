# Pods

Atomic unit of the smallest unit of work in K8s

Encapsulates an application container

Represent a unit of deployment

Pods can run one or more containers

> Containers within a pod share same IP space, mounted volumes

> Containers within a pod can communicate via localhost or IPC

Pods are ephemeral, short lived

Deploying a pod is an atomic operation, it either succeeds or not.

If a pod fails, it is replaced by a new pod with new IP address

> We don't update a pod, we replace the pod with an updated version

> We scale up by adding pods, not adding containers in pods
