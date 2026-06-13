# Cluster Upgrades

## Objective

Learn how Kubernetes clusters are upgraded while maintaining stability and availability.

## Overview

Kubernetes components should be upgraded in a controlled sequence.

Recommended order:

1. Control Plane Components
2. Worker Nodes

## Check Current Version

```bash
kubectl version

kubectl get nodes
```

## Upgrade Planning

```bash
kubeadm upgrade plan
```

This command displays available upgrade versions and required actions.

## Apply Upgrade

```bash
kubeadm upgrade apply v1.xx.x
```

## Upgrade Kubelet

```bash
apt-get update

apt-get install kubelet=<version>

systemctl restart kubelet
```

## Verify Upgrade

```bash
kubectl get nodes
```

## Key Learnings

- Control Plane should be upgraded first.
- Worker nodes can temporarily run an older version.
- Upgrades should be validated after each step.
- Always review upgrade plans before execution.
