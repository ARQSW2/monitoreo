# k8s Cluster logging

Logging a nivel de cluster con fluent-bit, Loki y Grafana

```bash
helm repo add grafana https://grafana.github.io/helm-charts

helm repo update grafana

helm upgrade --install loki grafana/loki-stack --set fluent-bit.enabled=true,promtail.enabled=false --namespace=monitoring  --create-namespace

```
