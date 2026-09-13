# 10 — Observability

## 💡 The three pillars

- **Metrics:** numerical measurements over time
- **Logs:** event records
- **Traces:** request journeys across components

## 🟢 Beginner

- Monitoring vs observability
- Metrics
- Logs
- Alerts
- Health checks
- Basic dashboards

## 🟡 Intermediate

- Prometheus
- Grafana
- Log aggregation
- Distributed tracing
- Labels and cardinality
- Alert design
- SLI/SLO/SLA

## 🔴 Advanced

- OpenTelemetry
- Instrumentation strategy
- Trace context propagation
- Sampling
- High-cardinality analysis
- Multi-cluster observability
- Security observability
- Correlating cloud, Kubernetes and application telemetry

## 🛠️ Lab

Create a service with:

```text
Application
 ├── Metrics → Prometheus → Grafana
 ├── Logs   → Log platform
 └── Traces → OpenTelemetry → Trace backend
```

Then deliberately introduce latency and errors and investigate the root cause.

## ⚫ Interview focus

- Monitoring vs observability
- Metrics vs logs vs traces
- What is an SLO?
- How do you avoid alert fatigue?
- What is distributed tracing?
- Why can high-cardinality metrics become expensive?
- How would you investigate intermittent latency?
