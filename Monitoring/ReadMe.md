# Monitoring 
### Monitoring Namespace
Create the monitoring namespace by using the command
`kubectl create namespace monitoring`

## Performance Metrics
### Prometheus Node Exporter
Create A Daemon Set using `kubectl apply -f node-exporter-ds.yml`
Create A ClusterIP Service using `kubectl apply -f node-exporter-service.yml`
Check that the service is successful `kubectl get endpoints -n monitoring`
This should have the same amount of endpoints as the amount of worker nodes