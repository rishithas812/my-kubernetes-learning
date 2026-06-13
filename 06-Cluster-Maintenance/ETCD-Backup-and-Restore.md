# ETCD Backup and Restore

## Objective

Learn how to back up and restore ETCD, the primary datastore of Kubernetes.

## Overview

ETCD stores all cluster state information including:

- Pods
- Deployments
- Services
- Secrets
- ConfigMaps
- Nodes

Without ETCD, Kubernetes cannot maintain cluster state.

## Create ETCD Snapshot

```bash
ETCDCTL_API=3 etcdctl snapshot save snapshot.db \
--endpoints=https://127.0.0.1:2379 \
--cacert=/etc/kubernetes/pki/etcd/ca.crt \
--cert=/etc/kubernetes/pki/etcd/server.crt \
--key=/etc/kubernetes/pki/etcd/server.key
```

## Verify Snapshot

```bash
etcdctl snapshot status snapshot.db
```

## Restore Snapshot

```bash
ETCDCTL_API=3 etcdctl snapshot restore snapshot.db
```

## Recovery Workflow

1. Stop ETCD service.
2. Restore snapshot.
3. Update ETCD configuration if required.
4. Restart ETCD.
5. Verify cluster health.

## Commands Practiced

```bash
etcdctl snapshot save snapshot.db

etcdctl snapshot status snapshot.db

etcdctl snapshot restore snapshot.db
```

## Key Learnings

- ETCD is the single source of truth for Kubernetes cluster state.
- Regular snapshots help reduce recovery time.
- Backup and recovery procedures should be tested periodically.
