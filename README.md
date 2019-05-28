# docker-compose-node

The easy starter project for node and docker compose

# Start container:

```
docker-compose up -d
```

-d: run container on background.

Check container is running or not:

```
docker ps
```

It is Ok if you will see the output like bellow:
```
CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS              PORTS                    NAMES
83731c902105        node:11             "npm start"         About a minute ago   Up About a minute   0.0.0.0:4100->3000/tcp   docker-compose-node_app_1
```

# Reload code after changing: 

We only need to restart container:

```
docker restart docker-compose-node_app_1

```

# Change port mapping:

We only change `ports` configuration in `docker-compose.yml` and run compose again:

```
nano docker-compose.yml
docker-compose up -d
```

If it is ok, you will see the output like below:

```
Recreating docker-compose-node_app_1 ... done
```
