# fabrikate-traefik-service

```
subcomponents:
  my-service:
    namespace: services
    config:
      gateway: my-ingress.istio-system.svc.cluster.local
      service:
        dns: myservice.mycompany.io
        name: my-service
        port: 80
      configMap:
        LOG_SEVERITY: "info"
        PORT: "80"
      image: "mycompany/mycontainer:433"
      replicas: 3
      port: 80
      resources:
        requests:
          cpu: "250m"
          memory: "256Mi"
        limits:
          cpu: "1000m"
          memory: "512Mi"
```
