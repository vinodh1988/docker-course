docker volume create <volume_name>
docker volume ls
docker volume inspect <volume_name>
docker volume rm <volume_name>
docker volume prune
docker run -v <volume_name>:<container_path> <image>
docker run --mount source=<volume_name>,target=<container_path> <image>
docker container run -v <volume_name>:<container_path> <image>
docker container run --mount source=<volume_name>,target=<container_path> <image>
docker compose up
docker compose down --volumes
docker system df --volumes
docker system prune --volumes

docker run --tmpfs <container_path> <image>
docker run --mount type=tmpfs,destination=<container_path> <image>
