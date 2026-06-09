# Scheduling

## Objective

The objective of this section was to understand how Kubernetes schedules Pods onto worker nodes and how administrators can influence scheduling decisions.

## Topics Covered

- Manual Scheduling
- Labels and Selectors
- Taints and Tolerations
- Node Selectors
- Node Affinity
- Resource Requests and Limits
- DaemonSets
- Static Pods
- Multiple Schedulers
- Priority Classes

## Summary

The Kubernetes Scheduler is responsible for determining where Pods should run within the cluster.

Scheduling decisions are based on:

- Resource availability
- Scheduling constraints
- Node characteristics
- Affinity rules
- Taints and tolerations

This section focused on understanding both the default scheduling behavior and administrator-controlled scheduling mechanisms.

## Key Learnings

- Scheduler assigns Pods to nodes.
- Labels help organize Kubernetes objects.
- Taints prevent Pods from running on specific nodes.
- Tolerations allow Pods to bypass taints.
- Affinity provides advanced scheduling controls.
- DaemonSets ensure one Pod runs on every node.

## References

- CKA Course – Scheduling
- Kubernetes Documentation
