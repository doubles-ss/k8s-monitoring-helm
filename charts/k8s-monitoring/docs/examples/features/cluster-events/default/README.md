<!--
(NOTE: Do not edit README.md directly. It is a generated file!)
(      To make changes, please modify values.yaml or description.txt and run `make examples`)
-->
# Cluster Events

This example demonstrates how to enable the Cluster Events feature to gather Kubernetes Cluster Events from the
Kubernetes API server and deliver them to a logs destination.

## Values

<!-- textlint-disable terminology -->
```yaml
---
cluster:
  name: cluster-events-cluster

destinations:
  - name: loki
    type: loki
    url: http://loki.loki.svc:3100/api/push

clusterEvents:
  enabled: true

alloy-singleton:
  enabled: true
```
<!-- textlint-enable terminology -->
