# Secrets

## Objective

Store sensitive information securely inside Kubernetes.

## Commands Used

Create Secret

```bash
kubectl create secret generic db-secret \
--from-literal=password=password123
```

View Secrets

```bash
kubectl get secrets
```

Describe Secret

```bash
kubectl describe secret db-secret
```

Delete Secret

```bash
kubectl delete secret db-secret
```

## Learning Outcome

- Secrets store confidential data.
- Data is stored as Base64 encoded values.
- Applications can consume secrets as environment variables or mounted files.
