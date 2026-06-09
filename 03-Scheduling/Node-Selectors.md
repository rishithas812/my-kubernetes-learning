# Node Selectors

## Objective

Understand how Pods can be scheduled on specific nodes using node selectors.

## Overview

Node selectors provide a simple way to control Pod placement.

First, label the node.

Example:

```bash
kubectl label node worker1 size=large
```

Then define the selector:

```yaml
spec:
  nodeSelector:
    size: large
```

## Commands Practiced

Add label:

```bash
kubectl label nodes worker1 size=large
```

Verify label:

```bash
kubectl get nodes --show-labels
```

## Limitations

Node selectors support only simple matching.

Complex scheduling requirements require Node Affinity.

## Key Learnings

- Easy scheduling mechanism.
- Based on node labels.
- Limited flexibility.
