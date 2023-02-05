# Instructions
This is a basic setup for a Minecraft server, pulled from the original Minecraft server docker image

When deploying this setup, docker compose maps the Minecraft server port 25565 to the same port of the host as specified in the compose file. The Minecraft client application can connect to this port directly. This example maps the Minecraft data folder holding all game storage to ~/minecraft_data on the host.
```bash
services:
 minecraft:
   image: itzg/minecraft-server
   ports:
     - "25565:25565"
    ...
  volumes:
     - "~/minecraft_data:/data"
```

# Deploying with docker compose 
This defines a volume for Minecraft server data to be stored, data can be recovered if you remove the container and restart it
```bash
$ mkdir -p ~/minecraft_data
$ docker compose up -d
WARNING: Some services (minecraft) use the 'deploy' key, which will be ignored. Compose does not support 'deploy' configuration - use `docker stack deploy` to deploy to a swarm.
Creating network "minecraft_default" with the default driver
Creating minecraft_minecraft_1 ... done
```

[original documentation](https://github.com/docker/awesome-compose/tree/master/minecraft)
