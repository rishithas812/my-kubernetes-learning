# Practice Commands

## Node Maintenance

```bash
kubectl cordon <node-name>

kubectl drain <node-name> --ignore-daemonsets

kubectl uncordon <node-name>
```

## Cluster Information

```bash
kubectl get nodes

kubectl version
```

## Upgrade Planning

```bash
kubeadm upgrade plan
```

## ETCD Backup

```bash
etcdctl snapshot save snapshot.db
```

## ETCD Verification

```bash
etcdctl snapshot status snapshot.db
```

## ETCD Restore

```bash
etcdctl snapshot restore snapshot.db
```

## Resource Export

```bash
kubectl get all --all-namespaces -o yaml > cluster-backup.yaml
```

## Notes

These commands were practiced while learning cluster maintenance activities including upgrades, node maintenance, backup creation, and recovery operations.
