# Metrics Server

## Objective

Understand the purpose of Metrics Server in Kubernetes.

## Overview

Metrics Server collects resource metrics from nodes and pods.

These metrics are used by:

- kubectl top
- Horizontal Pod Autoscaler (HPA)
- Monitoring solutions

## Architecture

Metrics flow:

Kubelet → Metrics Server → Kubernetes API

## Installation Verification

Check Metrics Server:

```bash
kubectl get deployment metrics-server -n kube-system
```

Check running pods:

```bash
kubectl get pods -n kube-system
```

## Commands Practiced

View node metrics:

```bash
kubectl top nodes
```

View pod metrics:

```bash
kubectl top pods
```

## Observations

Metrics Server provides near real-time resource utilization data.

## Key Learnings

- Metrics Server is not installed by default in all clusters.
- It collects CPU and memory metrics.
- Required for Horizontal Pod Autoscaling.
