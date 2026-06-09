# Manual Scheduling

## Objective

Understand how Pods can be scheduled manually without relying on the default Kubernetes Scheduler.

## Overview

Normally, Kubernetes Scheduler automatically assigns Pods to worker nodes.

However, Pods can also be scheduled manually by specifying the node name.

## Manual Scheduling Process

1. Create Pod without Scheduler.
2. Identify available node.
3. Assign Pod to node using `nodeName`.

Example:

```yaml
spec:
  nodeName: worker-node-1
```

## Use Cases

- Testing environments
- Learning scheduler behavior
- Troubleshooting scheduling issues

## Commands Practiced

```bash
kubectl get nodes
kubectl describe pod nginx
```

## Observations

When `nodeName` is specified, Kubernetes bypasses the scheduler and directly assigns the Pod to the selected node.

## Key Learnings

- Scheduler is not mandatory for Pod placement.
- `nodeName` forces Pod placement.
- Manual scheduling should be used carefully in production environments.
