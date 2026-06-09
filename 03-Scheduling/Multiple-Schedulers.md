# Multiple Schedulers

## Objective

Understand how Kubernetes supports multiple schedulers.

## Overview

Kubernetes provides a default scheduler.

Organizations can create custom schedulers for specialized workloads.

## Use Cases

- High-priority workloads
- GPU workloads
- Custom placement policies

## Scheduler Selection

Example:

```yaml
spec:
  schedulerName: custom-scheduler
```

## Commands Practiced

```bash
kubectl get pods
kubectl describe pod nginx
```

## Key Learnings

- Kubernetes supports custom schedulers.
- Pods can target specific schedulers.
- Useful for advanced workload management.
