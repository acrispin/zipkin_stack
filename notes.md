# Urls

## docker compose reference dokerfile
- https://stackoverflow.com/questions/32230577/how-do-i-define-the-name-of-image-built-with-docker-compose

## docker compose build
- https://docs.docker.com/compose/compose-file/

## install docker compose centos 7
- https://docs.docker.com/compose/install/

```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
``` 

## docker memory limits
- https://linuxhint.com/docker_compose_memory_limits/

## docker compose limit memory without deploy
- https://stackoverflow.com/questions/42457889/limit-useable-host-resources-in-docker-compose-without-swarm
- https://nickjanetakis.com/blog/docker-tip-78-using-compatibility-mode-to-set-memory-and-cpu-limits
```
$ docker-compose --compatibility up
```

## docker-compose set ARG docker file
- https://stackoverflow.com/questions/36738381/pass-a-variable-to-a-dockerfile-from-a-docker-compose-yml-file


## elasticsearch max virtual memory areas vm.max_map_count [65530] is too low
- https://discuss.opendistrocommunity.dev/t/max-virtual-memory-areas-max-map-count-65530-is-too-low/275
- https://github.com/elastic/elasticsearch-docker/issues/92
```
$ sudo sysctl -w vm.max_map_count=262144
```

## zipkin | spring sleuth
- https://zipkin.io/pages/quickstart
- https://stackabuse.com/spring-cloud-distributed-tracing-with-sleuth/
- https://github.com/openzipkin/zipkin/blob/master/docker/storage/elasticsearch7/README.md
- https://github.com/openzipkin/zipkin/tree/master/zipkin-server
- https://howtodoinjava.com/spring-cloud/spring-cloud-zipkin-sleuth-tutorial/

## zipkin Elasticsearch RabbitMQ docker
- https://github.com/openzipkin/zipkin/tree/master/docker
- https://www.jorgehernandezramirez.com/category/spring/springcloud/
- https://www.jorgehernandezramirez.com/2017/05/17/spring-cloud-sleuth-y-zipkin/


## install rabbitmq
- https://www.rabbitmq.com/download.html
``` 
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management
```

## zipkin elasticsearch remove old data | elasticsearch curator
- https://hub.docker.com/r/anjia0532/docker-curator
- https://github.com/anjia0532/docker-curator
- https://github.com/amoraes/zipkin-elasticsearch-cleaner
- https://www.elarraydejota.com/curator-eliminando-indices-de-elasticsearch/
- https://www.elastic.co/guide/en/elasticsearch/client/curator/current/fe_unit_count.html


## Cassandra version
- http://cassandra.apache.org/download/
- Download the latest Apache Cassandra 3.11 release: 3.11.6 (pgp, sha256 and sha512), released on 2020-02-14.
