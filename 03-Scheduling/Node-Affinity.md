# Node Affinity

## Objective

Learn advanced scheduling using Node Affinity.

## Overview

Node Affinity allows Pods to be scheduled based on node labels using flexible rules.

It improves upon Node Selectors.

## Types

### Required During Scheduling

Pod must run on matching node.

```yaml
requiredDuringSchedulingIgnoredDuringExecution
```

### Preferred During Scheduling

Kubernetes tries to place Pod on matching node.

```yaml
preferredDuringSchedulingIgnoredDuringExecution
```

## Example

```yaml
affinity:
  nodeAffinity:
    requiredDuringSchedulingIgnoredDuringExecution:
```

## Benefits

- Flexible scheduling
- Multiple matching rules
- Better workload placement

## Commands Practiced

```bash
kubectl describe pod nginx
kubectl get nodes --show-labels
```

## Key Learnings

- More powerful than node selectors.
- Supports complex scheduling requirements.
- Commonly used in production clusters.
