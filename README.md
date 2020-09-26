# Docker pi-hole

More docs can be found following these links,
- https://github.com/pi-hole/docker-pi-hole/
- https://hub.docker.com/r/pihole/pihole


## Start

```sh
# start container using docker-compose.yml (start/create detached)
docker-compose up -d

# check to make sure running (list containers)
docker ps

# Change DNS in network settings to 127.0.0.1 and ::1
```

A good way to check if pihole is running and is set up correctly is by going to the pihole admin dashboard, http://pi.hole/admin/

After the first time setting up, pihole can be started with
```sh
docker start pihole
```

## Stop

```sh
docker stop pihole
```

## Other Docker Cmds

```sh
# List containers (defaults to currently running containers)
docker container ls

# List all containers
docker container ls -a

# Alias for `docker container ls`
docker ps

# List images (defaults to hiding intermediatary images)
docker image ls

# List all images
docker image ls -a
```


## Customizations

The `DNS1` and `DNS2` environment variables are set to Cloudfares DNS.

If `WEBPASSWORD` is not set, a random one will be provided.
You can find this password by grepping the logs, `docker logs pihole | grep random` 

## Password
Nz0XXJyi

