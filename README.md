# docker-compose-examples
example of docker-compose configurations


## Tips:

### Enable interactive shell for a container

add the following:

```sh
stdin_open: true
tty: true
```

* `stdin_open` corresponds to `docker run -i ...`
* `tty` corresponds to `docker run -t ...`

### Get IP address of a running container:

Run in a terminal:

```sh
    docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' container_name_or_id
```