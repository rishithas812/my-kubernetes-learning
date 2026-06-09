# Cluster Architecture

## Objective

Understand the major components of a Kubernetes cluster and how they interact with each other.

## Components of a Kubernetes Cluster

A Kubernetes cluster consists of:

### Control Plane

The control plane manages the overall cluster state.

Components include:

- kube-apiserver
- etcd
- kube-scheduler
- kube-controller-manager

### Worker Nodes

Worker nodes run application workloads.

Components include:

- kubelet
- kube-proxy
- Container Runtime

## API Server

The API Server acts as the central management component of Kubernetes.

Responsibilities:

- Receives requests from users
- Validates requests
- Updates cluster state
- Communicates with ETCD

## ETCD

ETCD is a distributed key-value store used as the cluster database.

It stores:

- Nodes
- Pods
- Deployments
- Secrets
- ConfigMaps

## Scheduler

The scheduler determines which worker node should run a pod based on available resources and scheduling policies.

## Controller Manager

Controllers continuously monitor cluster state and ensure the desired state matches the actual state.

Examples:

- Node Controller
- Replication Controller
- Job Controller

## Commands Practiced

```bash
kubectl cluster-info
kubectl get nodes
```

## Key Learnings

- The API Server is the entry point to the cluster.
- ETCD stores cluster information.
- Scheduler makes placement decisions.
- Controllers continuously reconcile cluster state.

## References

- CKA Course - Cluster Architecture
- Kubernetes Documentation
