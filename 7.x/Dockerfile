FROM elasticsearch:7.4.1

ENV ES_VERSION=7.4.1
ENV AP_VERSION=7-4-1

# https://github.com/medcl/elasticsearch-analysis-ik/releases
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install -b https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v${ES_VERSION}/elasticsearch-analysis-ik-${ES_VERSION}.zip

ENV network.host=0.0.0.0
ENV cluster.name=es-${AP_VERSION}-cluster
ENV discovery.seed_hosts=es-${AP_VERSION}-discovery
ENV cluster.initial_master_nodes=es-${AP_VERSION}-0
