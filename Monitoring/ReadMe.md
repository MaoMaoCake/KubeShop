><!-- TOC -->
>* [Monitoring](#monitoring)
>    * [Monitoring Namespace](#monitoring-namespace)
>    * [Performance Metrics](#performance-metrics)
>    * [Prometheus Node Exporter](#prometheus-node-exporter)
>    * [Prometheus](#prometheus)
><!-- TOC -->

# Monitoring 
### Monitoring Namespace
Create the monitoring namespace by using the command
`kubectl create namespace monitoring`

### Performance Metrics
Current State:   
- Deploy node exporter  
- Deploy prometheus

To Do:
- Make prometheus persistent
- add Cadvisor

### Prometheus Node Exporter
Apply the node Exporter `kubectl apply -f Monitoring/PerformanceMetrics/NodeExporter`  
This should have the same amount of endpoints as the amount of worker nodes

### Prometheus
Apply prometheus `kubectl apply -f Monitoring/Core/Prometheus`  
This Should be applied last, so you don't need to restart prometheus