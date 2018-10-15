# What is vagrant_docker_swarm_hosts

```console
$ docker swarm init
```

```console
$ docker swarm join --token SWMTKN-1-5x0j19ksl7nlf0uo81nv52dvac0jyu44gpkb803xx53lc3nkhs-7mi255fezr7547qfhpv2vxcsh 192.168.0.101:2377
```

```console
$ docker network create -d macvlan --subnet=192.168.0.0/24 --gateway=192.168.0.1 -o parent=eth1 macvlan0
```

```console
$ ifconfig eth1 promisc
```

```console
docker run \
  --name='container1' \
  --hostname='container1' \
  --net=macvlan0 \
  --detach=true \
  --ip=192.168.0.23 \
  phusion/baseimage:latest
```
```console
Reply from 192.168.0.23: bytes=32 time<1ms TTL=64
```
