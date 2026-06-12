# Multi-Container Pods

## Objective

Understand scenarios where multiple containers run within the same Pod.

## Overview

A Pod can contain more than one container when containers need to work closely together.

Common patterns:

- Sidecar Pattern
- Adapter Pattern
- Ambassador Pattern

## Example

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: multi-container-pod
spec:
  containers:
  - name: web-app
    image: nginx

  - name: log-agent
    image: busybox
```

## Characteristics

- Shared Network Namespace
- Shared Storage Volumes
- Same Lifecycle

## Key Learnings

- Containers within a Pod communicate using localhost.
- Shared resources simplify integration.
- Sidecar containers are commonly used for logging and monitoring.
