
#FROM busybox:latest
FROM openjdk:8 
  
ENV LANG=C.UTF-8
  
RUN set -eux && mkdir -p /usr/skywalking/agent/
  
ADD apache-skywalking-apm-bin/agent/ /usr/skywalking/agent/
  
WORKDIR /
