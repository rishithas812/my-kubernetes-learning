# Deployments

## Objective

Learn how Deployments simplify application management.

## Overview

A Deployment provides declarative updates for applications.

It manages ReplicaSets and Pods.

## Features

- Rolling updates
- Rollbacks
- Scaling
- Version management

## Create Deployment

```bash
kubectl create deployment nginx --image=nginx
```

## View Deployments

```bash
kubectl get deployments

kubectl describe deployment nginx
```

## Scale Deployment

```bash
kubectl scale deployment nginx --replicas=5
```

## Rollout Status

```bash
kubectl rollout status deployment nginx
```

## Key Learnings

- Deployments are preferred over creating Pods directly.
- They provide update and rollback capabilities.
- Deployments manage ReplicaSets automatically.
