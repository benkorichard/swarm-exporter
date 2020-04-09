# swarm-exporter

A prometheus export which exports several metrics about a docker swarm cluster, e.g. node availability, number of running replicas of a service etc.

## Running

The exporter will need acccess to the docker API, it needs to run on a swarm manager node:
```shell
docker service create -v /var/run/docker.sock:/var/run/docker.sock -p 9515:9515 benkorichard/swarm-exporter
``` 
