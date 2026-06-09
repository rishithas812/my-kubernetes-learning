# Namespaces

## Objective

Understand how Kubernetes logically separates resources.

## Overview

Namespaces allow multiple teams, applications, or environments to share a cluster while remaining isolated.

Common namespaces:

- default
- kube-system
- kube-public
- kube-node-lease

## View Namespaces

```bash
kubectl get namespaces
```

## Create Namespace

```bash
kubectl create namespace dev
```

## Deploy Resource in Namespace

```bash
kubectl run nginx --image=nginx --namespace=dev
```

## Access Resources

```bash
kubectl get pods -n dev
```

## Key Learnings

- Namespaces provide logical separation.
- Useful for development, testing, and production environments.
- Resource quotas can be applied per namespace.
