# Commands and Arguments

## Objective

Understand how commands and arguments can be overridden when running containers in Kubernetes.

## Overview

Containers have default commands and arguments defined in their Docker image.

Kubernetes allows these values to be customized during Pod creation.

## Example

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: ubuntu-sleeper
spec:
  containers:
  - name: ubuntu
    image: ubuntu
    command: ["sleep"]
    args: ["300"]
```

## Verification

```bash
kubectl describe pod ubuntu-sleeper
```

## Key Learnings

- Commands override Docker ENTRYPOINT.
- Arguments override Docker CMD.
- Custom commands allow flexible container behavior.
