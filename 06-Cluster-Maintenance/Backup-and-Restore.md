# Backup and Restore

## Objective

Understand the different methods available for backing up Kubernetes resources and recovering them when needed.

## What Should Be Backed Up

Important cluster assets include:

- ETCD database
- YAML manifests
- Certificates
- Cluster configuration files

## Resource Backup

Export Kubernetes resources.

```bash
kubectl get all --all-namespaces -o yaml > cluster-backup.yaml
```

## Restore Resources

```bash
kubectl apply -f cluster-backup.yaml
```

## Backup Considerations

- Store backups securely.
- Automate backup schedules.
- Regularly test restore procedures.

## Key Learnings

- Backups are critical for disaster recovery.
- Resource manifests should be version controlled.
- Backup verification is as important as backup creation.
