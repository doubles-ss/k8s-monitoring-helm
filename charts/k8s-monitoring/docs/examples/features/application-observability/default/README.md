<!--
(NOTE: Do not edit README.md directly. It is a generated file!)
(      To make changes, please modify values.yaml or description.txt and run `make examples`)
-->
# Application Observability

This example shows how to enable the Application Observability feature, which enables the collection of application
telemetry data. Enabling this feature requires enabling one or more receivers where data will be sent from the
application.

For more information, see the [Application Observability feature documentation](https://github.com/grafana/k8s-monitoring-helm/tree/main/charts/k8s-monitoring/charts/feature-application-observability).

## Values

<!-- textlint-disable terminology -->
```yaml
---
cluster:
  name: applications-cluster

destinations:
  - name: otlp-gateway
    type: otlp
    url: http://otlp-gateway.example.com
    metrics: {enabled: true}
    logs: {enabled: true}
    traces: {enabled: true}

applicationObservability:
  enabled: true
  receivers:
    otlp:
      http:
        enabled: true

alloy-receiver:
  enabled: true
```
<!-- textlint-enable terminology -->
