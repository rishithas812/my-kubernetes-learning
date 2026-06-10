# Managing Application Logs

## Objective

Understand how application logs can be viewed and analyzed in Kubernetes.

## Overview

Logs provide information about application behavior and runtime events.

They are one of the primary tools used for troubleshooting.

## Viewing Logs

Display logs:

```bash
kubectl logs nginx
```

Display logs from a specific namespace:

```bash
kubectl logs -n default nginx
```

## Multi-Container Pods

Specify container name:

```bash
kubectl logs nginx -c sidecar
```

## Streaming Logs

Follow logs in real time:

```bash
kubectl logs -f nginx
```

## Observations

Logs are often the first place to investigate application failures.

## Key Learnings

- Logs help identify application issues.
- Logs can be viewed per container.
- Real-time log streaming is useful during debugging.
