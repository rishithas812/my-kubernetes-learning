# Environment Variables

## Objective

Learn how to provide configuration values to applications using environment variables.

## Overview

Environment variables allow applications to receive configuration without modifying application code.

## Example

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: app-pod
spec:
  containers:
  - name: app-container
    image: nginx
    env:
    - name: APP_MODE
      value: production
```

## Verify Environment Variables

```bash
kubectl exec app-pod -- env
```

## Key Learnings

- Environment variables separate configuration from code.
- Values can be hardcoded or sourced externally.
- Useful for application configuration and runtime settings.
