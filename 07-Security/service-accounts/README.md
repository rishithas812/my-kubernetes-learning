# Service Accounts

## Objective

Learn how applications running inside a pod authenticate with the Kubernetes API.

## Commands Used

```bash
kubectl get sa

kubectl create sa dashboard-sa

kubectl describe sa dashboard-sa
```

## Verification

```bash
kubectl get sa
```

Expected Output:

```text
NAME          SECRETS   AGE
default       1         10d
dashboard-sa  1         1m
```

## Learning Outcome

- Service Accounts are used by applications.
- Different from user accounts.
- Pods use service account tokens to communicate with Kubernetes API.
