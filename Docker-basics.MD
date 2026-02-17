### Case study1
### Create a Docker image which has pre installed jdk 17
#### preferabbly open

Steps

Any os image can be used as Base image

We are going to use

ubuntu

Image is going to be created manually

```
docker run -it ubuntu

In the terminal
root#   apt update -y
root# apt install openjdk-17-jdk -y
root# java --version
root# exit
```


docker commit containerid <yourdockerusenrmae>/imagename
docker push <yourdockerusername>/imagename