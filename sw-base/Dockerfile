
#FROM busybox:latest
FROM openjdk:8 

# MAINTAINER hbstarjason@gmail.com

ENV LANG=C.UTF-8
  
RUN set -eux && mkdir -p /usr/skywalking/agent/

# https://skywalking.apache.org/downloads/
# https://archive.apache.org/dist/skywalking/6.1.0/apache-skywalking-apm-6.1.0.tar.gz
ADD apache-skywalking-apm-bin/agent/ /usr/skywalking/agent/
  
WORKDIR /
