# Docker ROS2 - Humble
Docker created to be able to simulate the entire driving stack of the Formula Student Driverless university project, includes all the tools to be able to use ros foxy from the command line and created the docker image using the `docker-compose.yml` it is also possible to have graphical tools such as `rviz2` or `plotjuggler` by accessing to the docker via `ssh`

## docker-compose.yml
```yaml
services: 
  pc:
    build: .
    ports:
      - 2224:22
    volumes:
      - "/tmp/.X11-unix:/tmp/.X11-unix:rw"
```

## execute
```bash
$ docker compose up --build -d
$ ssh -p 2224 -Y mmr@localhost
```