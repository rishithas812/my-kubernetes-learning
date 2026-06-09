# DaemonSets

## Objective

Understand how DaemonSets ensure Pods run on every node.

## Overview

A DaemonSet automatically deploys one Pod on each node.

When a new node joins the cluster, the Pod is automatically created.

## Common Use Cases

- Log collection
- Monitoring agents
- Security agents
- Networking components

Examples:

- Fluentd
- Prometheus Node Exporter

## Commands Practiced

```bash
kubectl get daemonsets
kubectl describe daemonset <name>
```

## Observations

DaemonSets help ensure cluster-wide services run consistently across all nodes.

## Key Learnings

- One Pod per node.
- Automatically handles new nodes.
- Commonly used for infrastructure services.
