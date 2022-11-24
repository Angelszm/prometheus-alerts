## Prometheus-Alerts
https://prometheus.io/docs/introduction/overview/
Def: Time Series Database 

- Rules
- Alerting
- Metrics 




### Rules: 
```
nano rules.yaml
prometheus.yml (For Adding new rules in rule section)
systemctl restart prometheus or 
service prometheus restart
./promtool check rules rules/rules.yaml
```

Active alerts > ALERTS in metrics 



# Versions Different for every node groups
- Node Group Cluster Version (Should be all same)
- Should be test one dev or staging first 

- Prometheus and Grafana Dashboard 
- Should be dev and staging (Use Variables or may be use another public dashboard)
- Grafana Alerts should be same in each region (Or Use Alert Manager)

### Metrics 
- Node Exporter (Create metrics based on exporter)
- Or 

### Node Exporter 
- Need /metrics from daemonsets
- 
Install Node Exporter 
```

```

### Targets
- Database 


## Configuration

- basically need to create the rules on a configmap
- load the promethues pod with the configmap
- inject the prometheus config to read the file from the configmap


