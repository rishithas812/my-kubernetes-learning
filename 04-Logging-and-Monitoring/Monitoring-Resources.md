# Monitoring Resources

## Objective

Understand how to monitor resource consumption within the cluster.

## Overview

Resource monitoring helps ensure workloads receive sufficient CPU and memory.

Monitoring helps detect:

- High CPU usage
- Memory pressure
- Resource exhaustion
- Performance degradation

## Node Resource Monitoring

View node resource usage:

```bash
kubectl top nodes
```

Example output:

```text
NAME        CPU(cores)   MEMORY(bytes)
worker-1    120m         1024Mi
```

## Pod Resource Monitoring

View pod resource usage:

```bash
kubectl top pods
```

Example output:

```text
NAME      CPU(cores)   MEMORY(bytes)
nginx     15m          40Mi
```

## Observations

Resource monitoring helps identify applications that require optimization or scaling.

## Key Learnings

- CPU and memory are primary monitoring metrics.
- Resource consumption influences scheduling decisions.
- Monitoring supports capacity planning.
