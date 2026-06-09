# Resource Requests and Limits

## Objective

Understand how Kubernetes manages CPU and Memory allocation.

## Requests

Requests define the minimum resources required by a container.

Example:

```yaml
resources:
  requests:
    memory: "128Mi"
    cpu: "250m"
```

## Limits

Limits define the maximum resources a container can consume.

Example:

```yaml
resources:
  limits:
    memory: "256Mi"
    cpu: "500m"
```

## Benefits

- Prevent resource starvation
- Improve scheduling decisions
- Better cluster utilization

## Commands Practiced

```bash
kubectl describe pod nginx
```

## Observations

Scheduler uses resource requests when determining Pod placement.

## Key Learnings

- Requests affect scheduling.
- Limits prevent excessive resource consumption.
- Resource management is important in production environments.
