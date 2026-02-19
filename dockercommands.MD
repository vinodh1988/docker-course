
# Docker Custom Network Creation

## Create a Custom Network in 192.168.0.0 Address Space

```bash
docker network create --driver bridge --subnet 192.168.0.0/24 my-custom-network
```

### Parameters Explained
- `--driver bridge`: Uses bridge network driver
- `--subnet 192.168.0.0/24`: Defines the network address space
- `my-custom-network`: Name of the custom network

## Verify Network Creation

```bash
docker network ls
docker network inspect my-custom-network
```

## Connect a Container to the Custom Network

```bash
docker run -it --name my-container --network my-custom-network ubuntu
```

## Disconnect a Container from the Network

```bash
docker network disconnect my-custom-network my-container
```

## Remove the Custom Network

```bash
docker network rm my-custom-network
```

docker network create --driver bridge --subnet 192.168.0.0/24 mynetwork