FROM elasticsearch:7.4.0

ENV ES_VERSION=7.4.0
ENV AP_VERSION=7-4-0

# https://github.com/medcl/elasticsearch-analysis-ik/releases
ADD https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v$ES_VERSION/elasticsearch-analysis-ik-$ES_VERSION.zip /tmp/
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install -b file:///tmp/elasticsearch-analysis-ik-$ES_VERSION.zip

RUN rm -rf /tmp/*

ADD config /usr/share/elasticsearch/config

ENV CLUSTER_NAME=es-$AP_VERSION-cluster
ENV DISCOVERY_SERVICE=es-$AP_VERSION-discovery
ENV INITIAL_MASTERS=["node-1"]
