# Practice Commands

## Deployment Rollouts

```bash
kubectl rollout status deployment nginx-deployment

kubectl rollout history deployment nginx-deployment

kubectl rollout undo deployment nginx-deployment
```

## Deployment Updates

```bash
kubectl set image deployment nginx-deployment nginx=nginx:1.25
```

## ConfigMaps

```bash
kubectl create configmap app-config \
--from-literal=APP_MODE=production

kubectl get configmaps

kubectl describe configmap app-config
```

## Secrets

```bash
kubectl create secret generic app-secret \
--from-literal=password=myPassword123

kubectl get secrets

kubectl describe secret app-secret
```

## Environment Variables

```bash
kubectl exec app-pod -- env
```

## Pod Inspection

```bash
kubectl describe pod <pod-name>

kubectl get pods
```

## Notes

These commands were practiced during the Application Lifecycle Management section to understand application deployment, configuration management, security, and health monitoring within Kubernetes.
