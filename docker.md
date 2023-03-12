# Docker

## Useful Command

```sh
# Check if docker engine is running
$ docker info

# Build an image with a tag
$ docker build -f Dockerfile -t repo_name:tag_name .

# Run a container with an image by ID or Repo:Tag
#    --rm : container to be removed when exiting or when the daemon exits
#    -i   : keep STDIN open even if not attached
#    -t   : allocate a pseudo-tty
#    -d   : start in detached mode
$ docker run --rm -itd -v /host/path/to/map:/container/path docker_img

# Attach to a running container by ID or Name
$ docker attach docker_container

# Detach from a container:
#    Press Ctrl+P, followed by Ctrl+Q
```

## References

[Start Docker Daemon on WSL](https://blog.nillsf.com/index.php/2020/06/29/how-to-automatically-start-the-docker-daemon-on-wsl2/)
