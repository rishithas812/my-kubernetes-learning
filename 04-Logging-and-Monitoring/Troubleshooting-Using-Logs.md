# Troubleshooting Using Logs

## Objective

Learn how logs can be used to troubleshoot Kubernetes workloads.

## Overview

When applications fail, logs often provide the fastest way to determine the root cause.

Common issues include:

- Incorrect configuration
- Missing dependencies
- Failed database connections
- Application crashes

## Troubleshooting Workflow

### Step 1: Check Pod Status

```bash
kubectl get pods
```

### Step 2: Describe Pod

```bash
kubectl describe pod nginx
```

### Step 3: Review Logs

```bash
kubectl logs nginx
```

### Step 4: Check Previous Logs

```bash
kubectl logs nginx --previous
```

## Common Failure States

### CrashLoopBackOff

Application repeatedly crashes and restarts.

### ImagePullBackOff

Container image cannot be downloaded.

### Error

Application exits unexpectedly.

## Observations

Combining logs with resource and event information provides faster issue resolution.

## Key Learnings

- Logs are the primary troubleshooting tool.
- Previous logs help diagnose container crashes.
- Pod events and logs should be analyzed together.
