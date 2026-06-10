# Monitoring Cluster Components

## Objective

Understand how Kubernetes cluster components can be monitored.

## Overview

A Kubernetes cluster contains several components that require monitoring.

These include:

- Nodes
- Pods
- Deployments
- Control Plane Components

Monitoring helps identify:

- Resource bottlenecks
- Failed workloads
- Unhealthy nodes
- Capacity issues

## Important Metrics

### Node Metrics

- CPU Usage
- Memory Usage
- Disk Utilization

### Pod Metrics

- CPU Consumption
- Memory Consumption
- Restart Count

## Commands Practiced

View nodes:

```bash
kubectl get nodes
```

View pods:

```bash
kubectl get pods -A
```

Describe resources:

```bash
kubectl describe node <node-name>
```

## Observations

Monitoring should be performed continuously to identify issues before they impact applications.

## Key Learnings

- Monitoring provides visibility into cluster health.
- Resource utilization helps with capacity planning.
- Node and Pod metrics are commonly monitored.
