# Container Logs

## Objective

Understand how Kubernetes manages container logs.

## Overview

Every container generates logs during execution.

Kubernetes provides access to container logs through kubectl.

Logs include:

- Startup messages
- Application output
- Error messages
- Runtime events

## Commands Practiced

View logs:

```bash
kubectl logs <pod-name>
```

View previous container logs:

```bash
kubectl logs <pod-name> --previous
```

View logs from specific container:

```bash
kubectl logs <pod-name> -c <container-name>
```

## Troubleshooting Scenarios

### CrashLoopBackOff

Check previous logs:

```bash
kubectl logs nginx --previous
```

### Application Startup Failure

Inspect startup messages and configuration errors.

## Observations

Container logs are often sufficient to identify common application issues.

## Key Learnings

- Logs are stored per container.
- Previous container logs help diagnose crashes.
- Logging is a critical troubleshooting skill.
