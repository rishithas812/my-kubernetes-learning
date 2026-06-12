# Application Health Checks

## Objective

Understand how Kubernetes monitors application health and availability.

## Overview

Kubernetes uses probes to determine whether applications are functioning correctly.

Types of probes:

- Liveness Probe
- Readiness Probe
- Startup Probe

## Liveness Probe

Checks whether the application is still running correctly.

```yaml
livenessProbe:
  httpGet:
    path: /
    port: 80
```

## Readiness Probe

Determines whether the application is ready to receive traffic.

```yaml
readinessProbe:
  httpGet:
    path: /
    port: 80
```

## Startup Probe

Used for applications that require additional startup time.

```yaml
startupProbe:
  httpGet:
    path: /
    port: 80
```

## Key Learnings

- Liveness probes detect unhealthy applications.
- Readiness probes control traffic routing.
- Startup probes prevent premature restarts during initialization.
