# Static Pods

## Objective

Understand how Static Pods are managed directly by the kubelet.

## Overview

Unlike regular Pods, Static Pods are not created through the API Server.

They are managed directly by the kubelet running on a node.

## Characteristics

- Created from local manifest files.
- Managed by kubelet.
- Commonly used for control plane components.

## Manifest Location

Typical path:

```bash
/etc/kubernetes/manifests
```

## Commands Practiced

```bash
ps -ef | grep kubelet
```

```bash
kubectl get pods -A
```

## Observations

Control plane components in kubeadm clusters often run as Static Pods.

## Key Learnings

- Managed by kubelet.
- Independent of scheduler.
- Frequently used for cluster bootstrapping.
