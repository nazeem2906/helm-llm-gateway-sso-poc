# Grafana Dashboard

This repository includes a portfolio-ready Grafana dashboard for LiteLLM Gateway observability.

## Files

- `examples/grafana/litellm-gateway-dashboard.json`: importable Grafana dashboard JSON.
- `charts/litellm-gateway/templates/grafana-dashboard-configmap.yaml`: optional dashboard ConfigMap for Grafana sidecar provisioning.

## What it shows

- Requests per second
- Total requests
- Token throughput
- Estimated spend
- Error rate
- Latency p95
- Top models by requests
- Top users / keys by usage
- Spend by model
- Provider / model errors

The PromQL queries use metric-name regexes so the dashboard remains useful across LiteLLM versions. For production, tune the queries to the exact metric names and labels exposed by your LiteLLM deployment.
