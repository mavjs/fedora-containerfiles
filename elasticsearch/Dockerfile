FROM fedora:latest
MAINTAINER "Ye Myat Kaung (Maverick)" <mavjs@mavjs.org>

RUN dnf -y install java-1.8.0-openjdk-headless tar && \
    cd /tmp && \
    curl -O https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-1.6.0.tar.gz && \
    tar xvzf elasticsearch-1.6.0.tar.gz && \
    rm -f elasticsearch-1.6.0.tar.gz && \
    mv /tmp/elasticsearch-1.6.0 /elasticsearch && \
    dnf clean all

VOLUME ["/data"]

WORKDIR /data

CMD ["/elasticsearch/bin/elasticsearch"]

EXPOSE 9200
EXPOSE 9300
