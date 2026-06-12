# Secrets

## Objective

Learn how sensitive information is stored and managed in Kubernetes.

## Overview

Secrets store confidential information such as:

- Passwords
- API Keys
- Tokens
- Certificates

Unlike ConfigMaps, Secrets are intended for sensitive data.

## Create Secret

```bash
kubectl create secret generic app-secret \
--from-literal=password=myPassword123
```

## View Secrets

```bash
kubectl get secrets

kubectl describe secret app-secret
```

## Example Usage

```yaml
env:
- name: DB_PASSWORD
  valueFrom:
    secretKeyRef:
      name: app-secret
      key: password
```

## Key Learnings

- Secrets should be used for sensitive information.
- Applications can access Secrets through environment variables or volumes.
- Base64 encoding is used for storage representation.
