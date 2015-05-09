FROM fedora:latest
MAINTAINER "Ye Myat Kaung (Maverick)" <mavjs@mavjs.org>

RUN yum -y install java-1.8.0-openjdk-headless; yum clean all
RUN \
  cd /tmp && \
  curl -O https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-1.5.2.tar.gz && \
  tar xvzf elasticsearch-1.5.2.tar.gz && \
  rm -f elasticsearch-1.5.2.tar.gz && \
  mv /tmp/elasticsearch-1.5.2 /elasticsearch

VOLUME ["/data"]

WORKDIR /data

CMD ["/elasticsearch/bin/elasticsearch"]

EXPOSE 9200
EXPOSE 9300
