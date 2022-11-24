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
- Node Group Cluster Version (Should be all same) (If not, all dashboards and alerts will disapper again due to diff versions)
- Should be test one dev or staging first and then use the same to all other regions 
- Prometheus and Grafana Dashboard 
- Should be dev and staging (Use Variables for namespaces or may be use another public dashboard)
- Grafana Alerts should be same in each region (Or Use Alert Manager)
## Configuration
- Basically need to create the rules on a configmap (Add under data section)
- Load the promethues pod with the configmap
- Inject the prometheus config to read the file from the configmap

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


## Configmap 


```
- Data: Defines the prometheus.rules and prometheus.yaml content and passes their information at runtime to the config map.
- Prometheus.rules: Contains the alerting rules used to generate alerts on the basis of various conditions; e.g., out of memory, out of disk space, etc. In this case, we used high pod memory usage.
- Prometheus.yml: This file is used for configuring Prometheus. It defines scraping jobs and their instances, as well as which rule files to load. The prometheus.yaml file contains all the configuration information that would help to dynamically discover pods and services running in the Kubernetes cluster. 
```

Ref: 
https://github.com/Angelszm/prometheus-yaml
