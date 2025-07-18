ConfigMaps:
k apply -f alloy-loki-cm.yaml
k apply -f alloy-mimir-cm.yaml
k apply -f alloy-tempo-cm.yaml

Helm charts:

TRACES
helm install alloy-traces grafana/alloy -n alloy -f values.yaml
helm upgrade alloy-traces grafana/alloy -n alloy -f values.yaml
helm uninstall alloy-traces grafana/alloy -n alloy

METRICS
helm install alloy-metrics grafana/alloy -n alloy -f values.yaml
helm upgrade alloy-metrics grafana/alloy -n alloy -f values.yaml
helm uninstall alloy-metrics grafana/alloy -n alloy

LOGS
helm install alloy-logs grafana/alloy -n alloy -f values.yaml
helm upgrade alloy-logs grafana/alloy -n alloy -f values.yaml
helm uninstall alloy-logs grafana/alloy -n alloy