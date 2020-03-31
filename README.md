# elasticsearch-docker

5.x elasticsearch.yml

```
http.host: 0.0.0.0
transport.host: 0.0.0.0

cluster.name: ${CLUSTER_NAME}

discovery:
  zen:
    ping.unicast.hosts: ${DISCOVERY_SERVICE}
    minimum_master_nodes: ${NUMBER_OF_MASTERS}
```

6.x elasticsearch.yml

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

some bug with ik 7.4.0 for es 7.4.0
