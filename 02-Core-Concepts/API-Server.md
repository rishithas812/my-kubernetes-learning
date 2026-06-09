# API Server

## Objective

Understand the role of the Kubernetes API Server.

## Overview

The API Server is the central management component of Kubernetes.

Every interaction with the cluster passes through the API Server.

Examples include:

```bash
kubectl get pods

kubectl create deployment nginx
```

## Responsibilities

- Authentication
- Authorization
- Request validation
- Updating ETCD
- Exposing Kubernetes APIs

## Request Flow

1. User sends request using kubectl.
2. API Server validates request.
3. API Server updates ETCD.
4. Controllers and other components react to the changes.

## Key Learnings

- API Server is the front-end of Kubernetes.
- All cluster communication flows through it.
- It coordinates interactions between components.
