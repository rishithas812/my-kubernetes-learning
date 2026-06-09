# Priority Classes

## Objective

Understand workload prioritization in Kubernetes.

## Overview

Priority Classes allow critical workloads to receive scheduling preference.

Higher-priority Pods may preempt lower-priority Pods when resources are limited.

## Example

```yaml
apiVersion: scheduling.k8s.io/v1
kind: PriorityClass
metadata:
  name: high-priority
value: 100000
```

## Benefits

- Protect critical applications
- Better resource allocation
- Improved workload management

## Commands Practiced

```bash
kubectl get priorityclass
```

## Key Learnings

- Priorities influence scheduling decisions.
- Critical workloads can be protected.
- Useful in resource-constrained clusters.
