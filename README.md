## Prometheus and Grafana

* Prometheus official website: https://prometheus.io/
* Prometheus official documentation: https://prometheus.io/docs/introduction/overview/
* CAdvisor, Prometheus, Redis Setup: https://prometheus.io/docs/guides/cadvisor/

NOTE: Use my docker-compose.yml file to setup Prometheus, Grafana and CAdvisor.

* How zerodha uses Prometheus: https://zerodha.tech/blog/infra-monitoring-at-zerodha/
* How Uber using microservices: https://www.uber.com/en-IN/blog/microservice-architecture/
* Sysdig Prometheus: https://sysdig.com/blog/redis-prometheus/
* Thanos: https://thanos.io/
* Grafana: https://grafana.com/

* Grafana Dashboard: https://grafana.com/grafana/dashboards

* Grafana Node Exporter Dashboard: https://grafana.com/grafana/dashboards/1860

* Login to Grafana: http://localhost:3000
* Login to Prometheus: http://localhost:9090/graph
* Login to CAdvisor: http://localhost:8080

* Grafana Credentials: admin/admin

### How to setup?

* Clone the repo: `git clone <repo>`
* Run `docker-compose up` to start the containers.
* Run `docker-compose down` to stop the containers.

* Always see the logs of the containers: `docker-compose logs -f`



### Error 

* grafana exited with code 1
* node-exporter  | ts=2024-10-01T08:59:09.787Z caller=collector.go:169 level=error msg="collector failed" name=powersupplyclass duration_seconds=0.013652742 err="could not get power_supply class info: error obtaining power_supply class info: failed to read file \"/host/sys/class/power_supply/BAT0/current_now\": no such device"


### Solution 
```bash
sudo chown -R 472:472 ./grafana
```

