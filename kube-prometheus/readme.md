# Prometheus Kubernetes Operatos

El Prometheus Operator es un componente complejo, por ese motivo hay una implementacion simple denominada kube-prometheus que utilizaremos para ver el funcionamiento del monitoreo en kubernetes

## Instalacion

```bash
# agrega el repositorio de helm
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
# actualiza el catalogo de charts
helm repo update
# Inicializa un Operator de Prometheus y coloca sus componentes en el namespace monitoring
helm install monitoring prometheus-community/kube-prometheus-stack -n monitoring --create-namespace
```
## Dashboard nginx

Agrega un dashboard mas a grafana que monitorea el [nginx-prometheus-exporter](https://github.com/nginxinc/nginx-prometheus-exporter)

```bash
kubectl apply -f ./dashboards/nginx-dashboard.yaml -n monitoring
```

## Links

- <https://prometheus-operator.dev/>
- <https://github.com/prometheus-operator/kube-prometheus>
