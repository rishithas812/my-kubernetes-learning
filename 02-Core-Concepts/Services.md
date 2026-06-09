# Services

## Objective

Understand how Services enable communication with Pods.

## Overview

Pods are temporary and their IP addresses can change.

Services provide a stable endpoint for accessing applications.

## Types of Services

### ClusterIP

Default service type.

Accessible only within the cluster.

### NodePort

Exposes an application on a port of the worker node.

### LoadBalancer

Exposes applications externally through a cloud provider load balancer.

## Create Service

```bash
kubectl expose pod nginx --port=80
```

## View Services

```bash
kubectl get svc
```

## Key Learnings

- Services provide stable networking.
- They enable communication between applications.
- Services decouple clients from pod IP changes.
