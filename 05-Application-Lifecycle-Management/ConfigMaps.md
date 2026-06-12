# ConfigMaps

## Objective

Understand how Kubernetes stores and manages application configuration data.

## Overview

ConfigMaps store non-sensitive configuration data as key-value pairs.

Applications can consume ConfigMaps as:

- Environment Variables
- Command-line Arguments
- Mounted Files

## Create ConfigMap

```bash
kubectl create configmap app-config \
--from-literal=APP_MODE=production
```

## View ConfigMaps

```bash
kubectl get configmaps

kubectl describe configmap app-config
```

## Example Usage

```yaml
envFrom:
- configMapRef:
    name: app-config
```

## Key Learnings

- ConfigMaps help centralize configuration management.
- Changes can be managed independently of application images.
- Suitable for non-sensitive configuration data.
