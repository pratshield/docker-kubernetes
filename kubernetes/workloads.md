# Workloads

A workload is an application running on Kubernetes

  - Pod: A pod is an atomic workload which represents a set of running containers
  - **ReplicaSet** 
  - **Deployment**
  - StatefulSet
  - DaemonSet
  - Tasks that run to cpmpletion
      - Job
      - CronJob

## ReplicaSet

- Primary method of managing pod replicas and their lifecycle to provide self healing capabilities
- Their job is to always ensure that the desired pods are always running
- While you can create ReplicaSets, the recommended way is to use Deployment

### kubectl replicaset cheat sheet
- ```kubectl apply -f <definition.yaml>``` CReate ReplicaSet
- ```kubectl get rs``` List ReplicaSets
- ```kubectl describe rs <rsName>``` Get info
- ```kubectl delete -f <definition.yaml>``` Delete the rs
- ```kubectl delete rs <rsName>``` Delete rs using name


## Deployment

- A deplyment manage a single pod template
- You create a deployment for each microservice

> Pods don't self heal, scale, updates and rollback but deployments can

> Deployments create ReplicaSets in the background and we don't need to interact with ReplicaSets directly

### deployment kubectl cheat sheet
- ```kubectl create deploy <deployName> --image=nginx --replicas=3 --port=80``` Create deployment imperatively
- ```kubectl apply -f <definition.yaml>``` CReate a deployment declaratively
- ```kubectl get deploy``` List deployments
- ```kubectl describe deploy <deployName> ``` Get info
- ```kubectl delete -f <definition.yaml>``` Delete the deployment
- ```kubectl delete deploy <deployName>``` Delete deployment using name
