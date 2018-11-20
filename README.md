This repo is based on [@https://github.com/graphite-project/docker-graphite-statsd](https://github.com/graphite-project/docker-graphite-statsd). (Release 1.1.4-10)

## Updates to original repo

- Modified `collectd.conf` to check server metrics or curl json from web link. 
- `docker-compose.yml` deploy as a stack on docker swarm.
- Dependencies add in Dockerfile to allow collectd's plugins to work. (collectd plugins used: df, curl_json)

## Prerequisites: 

- Ubuntu 18.04 LTS on GCE
- Docker swarm, refer to https://github.com/cquan808/docker-swarm-gcepd
- Grafana

## Quick start:

Clone this repo:

`git clone https://github.com/cquan808/docker-graphite-collectd.git`

Change into directory:

`cd docker-graphite-collectd/`

Build Dockerfile:

`docker build -t docker-graphite-collectd:latest .` 

Deploy Stack:

`docker stack deploy -c docker-compose.yml stack`

Check stack and services are up and running:

`docker stack ls`

`docker service ls`

`docker service logs stack_collectd-graphite`
