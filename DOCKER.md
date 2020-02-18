# Docker Commands

## Deleting all the containers

Before deleting the volumes, you need to delete all the existing containers using the following command (make sure the application is not running)

```bash
docker rm $(docker ps -a -q) -f
```

## Deleting all the volumes

Once all the containers are deleted, you can delete all the Docker volumes on your computer using the following command

```bash
docker volume prune
```

If you don't want to delete all the Docker volumes on your computer, you can search for a specific one and deleting it

```bash
docker volume ls
docker volume rm <name_of_volume>
```

## Recreating the volumes

Recreating the volumes is as simple as restarting the application

```bash
docker-compose up --build
```
