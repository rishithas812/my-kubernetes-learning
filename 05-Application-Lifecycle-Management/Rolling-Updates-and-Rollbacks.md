# Rolling Updates and Rollbacks

## Objective

Understand how Kubernetes performs application updates with minimal downtime and how failed deployments can be rolled back.

## Overview

Deployments allow applications to be updated gradually without affecting all running instances at once.

Kubernetes creates new Pods while terminating old Pods in a controlled manner.

## Check Deployment Status

```bash
kubectl rollout status deployment nginx-deployment
```

## Deployment History

```bash
kubectl rollout history deployment nginx-deployment
```

## Rollback Deployment

```bash
kubectl rollout undo deployment nginx-deployment
```

## Update Image

```bash
kubectl set image deployment nginx-deployment nginx=nginx:1.25
```

## Key Learnings

- Rolling updates reduce downtime.
- Kubernetes updates Pods gradually.
- Rollbacks help recover from failed releases.
- Deployment history can be used to track changes.
