# ETCD

## Objective

To understand the role of ETCD in a Kubernetes cluster.

## Overview

ETCD is a distributed key-value datastore used by Kubernetes to store cluster information.

It is considered the source of truth for the cluster.

## Information Stored in ETCD

- Nodes
- Pods
- Services
- Deployments
- Secrets
- ConfigMaps
- Cluster configuration

## Characteristics

- Distributed
- Highly available
- Consistent
- Reliable

## ETCD Backup

Since ETCD stores critical cluster information, regular backups are important.

Backup and restore procedures are common tasks for Kubernetes administrators.

## Commands Discussed

```bash
etcdctl snapshot save snapshot.db

etcdctl snapshot restore snapshot.db
```

## Key Learnings

- ETCD stores all cluster-related information.
- Losing ETCD can result in loss of cluster state.
- Backup and recovery are critical administrative tasks.
