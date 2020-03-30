FROM elasticsearch:7.4.0

ENV ES_VERSION=7.4.0
ENV AP_VERSION=7-4-0

# https://github.com/medcl/elasticsearch-analysis-ik/releases
ADD https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v$ES_VERSION/elasticsearch-analysis-ik-$ES_VERSION.zip /tmp/
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install file:///tmp/elasticsearch-analysis-ik-$ES_VERSION.zip

RUN rm -rf /tmp/*

ENV network.host=0.0.0.0
ENV cluster.name=es-$AP_VERSION-cluster
ENV discovery.seed_hosts=es-$AP_VERSION-discovery
ENV cluster.initial_master_nodes=es-$AP_VERSION-0
