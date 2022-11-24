## Prometheus-Alerts
https://prometheus.io/docs/introduction/overview/

Why Prometheus ? 
- Open Source Container Monitoring System
- Time Series Database 
- Rules
- Alerting
- Metrics 
- Query capabilities 
- Visualization 
Prometheus Query Language: (PromQL)



### Rules: 
```
nano rules.yaml
prometheus.yml (For Adding new rules in rule section)
systemctl restart prometheus or 
service prometheus restart
./promtool check rules rules/rules.yaml
```

Active alerts > ALERTS in metrics 



### Versions Different for every node groups
- Node Group Cluster Version (Should be all same)
- Should be test one dev or staging first 

- Prometheus and Grafana Dashboard 
- Should be dev and staging (Use Variables or may be use another public dashboard)
- Grafana Alerts should be same in each region (Or Use Alert Manager)

### Metrics 
- Node Exporter (Create metrics based on exporter)


### Node Exporter 
Means to fetch metrics
- Need/run /metrics from daemonsets


Install Node Exporter 
```
May be install node_exporter zip file or use node_exporter as service on k8s
```

### Targets
- Database 
- Jobx 
- Exporters


## Configuration
- basically need to create the rules on a configmap
- load the promethues pod with the configmap
- inject the prometheus config to read the file from the configmap


## Configmap 



Ref: 
https://github.com/Angelszm/prometheus-yaml
