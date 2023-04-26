# grafana_dashboards collection

## Can be integrated to grafana using the following configuration:

```yaml
  # Provision grafana-dashboards-kubernetes
  dashboardProviders:
    dashboardproviders.yaml:
      apiVersion: 1
      providers:
      - name: 'grafana-dashboards-kubernetes'
        orgId: 1
        folder: 'Kubernetes'
        type: file
        disableDeletion: true
        editable: true
        options:
          path: /var/lib/grafana/dashboards/grafana-dashboards-kubernetes
  dashboards:
    grafana-dashboards-kubernetes:
      k8s-system-api-server:
        url: $GIT_URL_YOU_HAVE
        token: ''
```

