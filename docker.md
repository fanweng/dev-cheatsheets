# Docker

## Useful Command

```sh
# Check if docker engine is running
$ docker info

# Build an image with a tag
#   /path : specify the path to the context, where it searches the Dockerfile
$ docker build -f Dockerfile -t repo_name:tag_name /path

# Run a container with a docker_img by ID or Repo:Tag
#    --rm : container to be removed when exiting or when the daemon exits
#    -i   : keep STDIN open even if not attached
#    -t   : allocate a pseudo-tty
#    -d   : start in detached mode
#    -p   : bind container port to host machine port
#           localhost IP 127.0.0.1 is default for host_port if not specified
$ docker run --rm -itd -v /host/path/to/map:/container/path -p host_port:container_port docker_img

# Show containers
$ docker ps
# Or,
$ docker container ls

# Attach to a running container by ID or Name
$ docker attach docker_container

# Detach from a container:
#    Press Ctrl+P, followed by Ctrl+Q

# Show logs from a container
$ docker logs container_id_or_name
# Continuously show logs
$ docker logs container_id_or_name -f

# Stop a container
$ docker stop container_id_or_name

# Run command outside the docker environment
# Really useful if the prompt isn't available in the docker environment
$ docker exec -d container_id_or_name your_cmd
```

## Official Images

In the Docker Hub, there are tons of officially built images that can be used directly. For example, to use [Ubuntu Lunar release](https://hub.docker.com/_/ubuntu/tags), search for `ubuntu` as the **repository**, go to the **tag** page and find the release `lunar-20230314`. 

We can specify the `FROM repo:tag` in the `Dokcerfile` so the build stage will pull that image.

```sh
$ cat Dockerfile
FROM ubuntu:lunar-20230314
```

## References

[Start Docker Daemon on WSL](https://blog.nillsf.com/index.php/2020/06/29/how-to-automatically-start-the-docker-daemon-on-wsl2/)
