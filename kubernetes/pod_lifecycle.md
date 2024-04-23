# Pod lifecycle

## Pod creation lifecycle
```mermaid

flowchart LR
  A(CLI)
  B(API Server)
  C(etcd)
  D(Scheduler)
  E(Kubelet)
  F(runtime)
  A-->|Cli create pod| B
  B-->|write| C
  
```
