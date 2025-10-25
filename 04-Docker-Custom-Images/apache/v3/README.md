## Docker Build Commands.

```
  138  mkdir 04-Docker-Custom-Images/apache/v1 -p
  139  ls
  140  cd 04-Docker-Custom-Images/apache/v1/
  141  ls
  142  vim Dockerfile
  143  ls
  144  docker build -t myapache:v1 .
  145  docker images
  146  docker inspect 8cbef15694e2
  147  docker history  8cbef15694e2
  148  docker images
  149  docker run -d --name myapache-test-1 myapache:v1
  150  docker ps
  151  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  152  curl 172.17.0.2
```
