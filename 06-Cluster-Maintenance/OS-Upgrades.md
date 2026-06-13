# Operating System Upgrades

## Objective

Understand how node maintenance is performed without impacting application availability.

## Overview

Worker nodes require periodic operating system upgrades to apply security patches and system updates.

Before performing maintenance, workloads running on the node should be safely moved to other available nodes.

## Cordon a Node

Mark a node as unschedulable.

```bash
kubectl cordon <node-name>
```

No new Pods will be scheduled on this node.

## Drain a Node

Evict existing workloads from the node.

```bash
kubectl drain <node-name> --ignore-daemonsets
```

The scheduler moves workloads to other nodes if resources are available.

## Uncordon a Node

Make the node schedulable again.

```bash
kubectl uncordon <node-name>
```

## Commands Practiced

```bash
kubectl cordon worker-node

kubectl drain worker-node --ignore-daemonsets

kubectl uncordon worker-node
```

## Key Learnings

- Cordon prevents new Pods from being scheduled.
- Drain safely removes workloads before maintenance.
- Uncordon restores normal scheduling behavior.
- Maintenance operations should be planned to minimize disruption.
