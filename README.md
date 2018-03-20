# Cassandra Spring-boot

- run cassandra docker container

`docker run --name cassandra -p 7000:7000 -p 7001:7001 -p 7199:7199 -p 9042:9042 -p 9160:9160 -d cassandra`

- connect cqlsh client to docker cassandra

`docker run -it --link cassandra:cassandra --rm cassandra cqlsh cassandra`

- create keyspace

`CREATE KEYSPACE test WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 2};`

- run spring boot app

`mvn spring-boot:run`