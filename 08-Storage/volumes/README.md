# Volumes

## Objective

Understand how data can persist within a pod using Kubernetes volumes.

## Commands Used

```bash
kubectl apply -f pod-volume.yaml

kubectl get pods

kubectl describe pod web-pod
```

## Verification

```bash
kubectl describe pod web-pod
```

## Learning Outcome

* Volumes provide storage to containers.
* Data survives container restarts within the same pod.
* Multiple containers in a pod can share a volume.
