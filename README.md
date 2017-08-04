# dcos-kafka-docker
DCOS docker to deploy kafka in a scalable fashion.

It needs a HOST network and 2 assigned ports.

## Configurable options:

Zookeeper address for your DCOS cluster goes into an environment variable:
```KAFKA_ZOOKEEPER_CONNECT```

You can modify the kafka version here in the Dockerfile:
```
ENV KAFKA_VERSION="0.10.2.1" SCALA_VERSION="2.11"
```

You can add kafka-broker options in the kafka-marathon-bootstrap.sh script, just add lines like this:
```
echo "port=${PORT0}" >> $KAFKA_HOME/config/custom-server.properties
```
