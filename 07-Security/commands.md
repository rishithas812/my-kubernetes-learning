# Security Commands

## Service Accounts

```bash
kubectl get sa

kubectl create sa dashboard-sa

kubectl describe sa dashboard-sa
```

---

## Secrets

```bash
kubectl get secrets

kubectl create secret generic db-secret \
--from-literal=password=password123

kubectl describe secret db-secret

kubectl delete secret db-secret
```

---

## RBAC

```bash
kubectl get roles

kubectl get rolebindings

kubectl get clusterroles

kubectl get clusterrolebindings
```

---

## Certificates

```bash
openssl x509 -in apiserver.crt -text -noout

openssl rsa -in apiserver.key -check
```

---

## Network Policies

```bash
kubectl get networkpolicies

kubectl describe networkpolicy
```
