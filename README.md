# docker-swarm-proxy

What if you wanted a docker exec, but for Docker swarm?

This project allows you to control any docker engine in the swarm from a manager (or your local computer if you use SSH proxying).

![grafik](https://github.com/neuroforgede/docker-swarm-proxy/assets/719760/33294423-a874-47ac-86c9-529c39b5f78b)

## Installation

Install to your docker cli (from github)

```bash
rm ~/.docker/cli-plugins/docker-swarmproxy
curl -L https://raw.githubusercontent.com/neuroforgede/docker-swarm-proxy/master/docker_swarm_proxy.py -o ~/.docker/cli-plugins/docker-swarmproxy
chmod +x ~/.docker/cli-plugins/docker-swarmproxy
```

Or copy from a local copy:

```bash
cp docker_swarm_proxy.py ~/.docker/cli-plugins/docker-swarmproxy
chmod +x ~/.docker/cli-plugins/docker-swarmproxy
```

## Usage

### Exec into a running service

```bash
docker swarmproxy service exec -it vibrant_bell bash
```

See all available options:

```bash
docker swarmproxy service exec --help
```