# elasticsearch-docker

5.x 
https://www.elastic.co/guide/en/kibana/5.5/settings.html
elasticsearch.yml

```
http.host: 0.0.0.0
transport.host: 0.0.0.0

cluster.name: ${CLUSTER_NAME}

discovery:
  zen:
    ping.unicast.hosts: ${DISCOVERY_SERVICE}
    minimum_master_nodes: ${NUMBER_OF_MASTERS}
```

6.x 
https://www.elastic.co/guide/en/kibana/6.7/settings.html
elasticsearch.yml

```
http.host: 0.0.0.0
transport.host: 0.0.0.0

cluster.name: ${CLUSTER_NAME}

discovery:
  zen:
    ping.unicast.hosts: ${DISCOVERY_SERVICE}
    minimum_master_nodes: ${NUMBER_OF_MASTERS}
```

7.x
https://www.elastic.co/guide/en/kibana/7.4/settings.html
some bug with ik 7.4.0 for es 7.4.0
