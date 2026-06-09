# Pods

## Objective

Understand Pods, the smallest deployable unit in Kubernetes.

## Overview

A Pod is the smallest object that Kubernetes creates and manages.

Containers are not deployed directly in Kubernetes. They are deployed inside Pods.

## Pod Structure

Pod
└── Container

In most production environments, a pod contains a single container.

## Pod Lifecycle

### Pending

Pod has been accepted but is not yet running.

### Running

Pod is running successfully.

### Succeeded

Pod completed its task successfully.

### Failed

Pod terminated due to an error.

### Unknown

Pod state cannot be determined.

## Create a Pod

```bash
kubectl run nginx --image=nginx
```

## View Pods

```bash
kubectl get pods

kubectl describe pod nginx
```

## Delete a Pod

```bash
kubectl delete pod nginx
```

## Key Learnings

- Pods are the smallest deployable unit.
- Containers always run inside Pods.
- Pods are temporary and can be recreated by controllers.
