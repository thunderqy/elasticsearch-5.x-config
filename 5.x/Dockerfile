ARG ES_VERSION=5.6.16-alpine
ARG IK_VERSION=5.6.16
ARG AP_VERSION=5-6-16

FROM elasticsearch:$ES_VERSION

# https://github.com/medcl/elasticsearch-analysis-ik/releases
ADD https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v${IK_VERSION}/elasticsearch-analysis-ik-$IK_VERSION.zip /tmp/
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install file:///tmp/elasticsearch-analysis-ik-$IK_VERSION.zip

RUN rm -rf /tmp/*

ADD config /usr/share/elasticsearch/config

ENV CLUSTER_NAME=$AP_VERSION-cluster
ENV DISCOVERY_SERVICE=$AP_VERSION-discovery
ENV NUMBER_OF_MASTERS=1
