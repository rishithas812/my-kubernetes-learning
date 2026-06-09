# Taints and Tolerations

## Objective

Understand how Kubernetes controls Pod placement using taints and tolerations.

## Taints

Taints are applied to nodes.

They prevent Pods from being scheduled unless the Pod has a matching toleration.

Syntax:

```bash
kubectl taint nodes node1 key=value:NoSchedule
```

Example:

```bash
kubectl taint nodes worker1 app=database:NoSchedule
```

## Tolerations

Tolerations are added to Pods.

Example:

```yaml
tolerations:
- key: "app"
  operator: "Equal"
  value: "database"
  effect: "NoSchedule"
```

## Taint Effects

### NoSchedule

Pod will not be scheduled.

### PreferNoSchedule

Kubernetes tries to avoid scheduling.

### NoExecute

Existing Pods may be evicted.

## Commands Practiced

```bash
kubectl describe node worker1
kubectl taint nodes worker1 app=database:NoSchedule
```

## Observations

Taints alone do not force Pods onto nodes.

They only restrict placement.

## Key Learnings

- Taints are configured on nodes.
- Tolerations are configured on Pods.
- They work together to control scheduling.
