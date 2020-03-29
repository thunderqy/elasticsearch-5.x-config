FROM elasticsearch:5.6.16-alpine

ENV VERSION=5.6.16

# https://github.com/medcl/elasticsearch-analysis-ik/releases
ADD https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v${VERSION}/elasticsearch-analysis-ik-$VERSION.zip /tmp/
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install file:///tmp/elasticsearch-analysis-ik-$VERSION.zip

RUN rm -rf /tmp/*

ADD config /usr/share/elasticsearch/config

ENV CLUSTER_NAME=es-5-6-16-cluster
ENV DISCOVERY_SERVICE=es-5-6-16-discovery
ENV NUMBER_OF_MASTERS=1
