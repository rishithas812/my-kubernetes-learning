# ReplicaSets

## Objective

Understand how Kubernetes maintains a desired number of pod replicas.

## Overview

A ReplicaSet ensures that a specified number of pod replicas are running at all times.

If a pod fails, the ReplicaSet automatically creates a replacement.

## Benefits

- High availability
- Self-healing
- Automatic pod replacement

## Common Commands

```bash
kubectl get rs

kubectl describe rs
```

## Example

Desired Replicas: 3

Current Running Pods: 2

ReplicaSet creates 1 additional pod.

## Key Learnings

- ReplicaSets maintain pod availability.
- They continuously monitor running pods.
- Deployments manage ReplicaSets.
