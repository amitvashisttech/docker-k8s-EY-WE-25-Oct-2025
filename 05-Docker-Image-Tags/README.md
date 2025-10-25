```

  260  cd 05-Docker-Image-Tags/
  261  ls
  262  docker images
  263  docker login
  264  docker login -u amitvashist7
  265  ls
  266  docker images
  267  docker push myapache:v1
  268  docker tag myapache:v1 amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v1
  269  docker images
  270  docker push amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v1
  271  docker tag myapache:v2 amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v2
  272  docker tag myapache:v3 amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v3
  273  docker tag myapache:v4 amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v4
  274  docker images
  275  docker push amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v2
  276  docker push amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v3
  277  docker push amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v4
  278  ls
  279  docker logout
  280  docker kill  $(docker ps -q)
  281  docker rm  $(docker ps -qa)
  282  docker rmi $(docker images -q)
  283  docker rmi $(docker images -q) --force
  284  docker images
  285  docker run -d  amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v4
  286  docker ps
  287  curl 172.17.0.2
  288  docker tag myapache:v4 amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:latest
  289  docker tag amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v4 amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:latest
  290  docker images

```
