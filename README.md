# skywalking-k8s
docker build -t hbstarjason/sw-base:6.1.0 .



# 安装

```bash
# http://skywalking.apache.org/

$ mkdir work && cd work && \
    git init && \
    git remote add -f origin https://github.com/apache/skywalking-kubernetes.git && \
    git config core.sparsecheckout true && \
    echo skywalking >> .git/info/sparse-checkout && \
    git pull origin master
    
$ curl -sSL https://get.helm.sh/helm-v3.2.4-linux-amd64.tar.gz |  sudo tar xz -C /usr/local/bin --strip-components=1 linux-amd64/helm

$ helm repo add elastic https://helm.elastic.co/

$ helm repo up && \
  helm dep up ./chart/skywalking/ && \
  helm lint ./chart/skywalking/

$ kubectl create ns skywalking-es7
$ helm -n skywalking-es7 install skywalking ./chart/skywalking \
        --set oap.replicas=1 --set elasticsearch.replicas=1
```

