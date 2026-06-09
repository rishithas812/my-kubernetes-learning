# Labels and Selectors

## Objective

Understand how Labels and Selectors are used to organize and identify Kubernetes objects.

## Labels

Labels are key-value pairs attached to Kubernetes resources.

Example:

```yaml
labels:
  app: nginx
  environment: production
```

## Benefits

- Resource organization
- Filtering resources
- Service-to-Pod mapping
- Deployment management

## Selectors

Selectors are used to identify resources based on labels.

Example:

```yaml
selector:
  app: nginx
```

## Commands Practiced

View labels:

```bash
kubectl get pods --show-labels
```

Filter Pods:

```bash
kubectl get pods -l app=nginx
```

## Observations

Services and Deployments rely heavily on labels and selectors for resource management.

## Key Learnings

- Labels identify resources.
- Selectors find resources.
- Most Kubernetes objects use labels internally.
