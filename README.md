# Grafana4IoT

Easily hook up your Watson IoT organization to grafana to generate powerful visualizations and 
dashboards quickly and easily.  Works great in conjunction with the [Watson IoT Connector for statsd](https://github.com/ibm-watson-iot/connector-statsd).

## Usage
The easiest way to use this project is with [Docker Compose](https://www.docker.com/products/docker-compose).  The default compose file will launch a single instance of the statsd connector and grafana4iot.  Additional connectors can be deployed to bring data from multiple organizations into grafana.

```
[root@localhost ~]# export IOT_API_KEY=<your api key>
[root@localhost ~]# export IOT_API_TOKEN=<your auth token>
[root@localhost ~]# wget https://github.com/ibm-watson-iot/grafana4iot/blob/master/docker-compose.yml
[root@localhost ~]# docker-compose up
```

To update an existing instance of the service:
```
[root@localhost ~]# wget https://github.com/ibm-watson-iot/grafana4iot/blob/master/docker-compose.yml
[root@localhost ~]# docker-compose build && docker-compose up -d
```
