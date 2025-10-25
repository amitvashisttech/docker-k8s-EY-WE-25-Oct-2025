```
 299  docker ps
  300  docker kill  $(docker ps -qa)
  301  docker network ls
  302  docker ps
  303  docker run -itd ubuntu
  304  docker ps
  305  docker inspect dd8cec20a462
  306  docker network ls
  307  docker network inspect 328a83e77768
  308  ifconfig
  309  route -n
  310  docker ps
  311  docker run -it ubuntu
  312  ls
  313  docker ps
  314  docker run -d --name test-web-1 nginx
  315  docker ps
  316  curl 172.17.0.4
  317  ip a
  318  curl 10.0.8.126
  319  docker run -d --name test-web-2 -P nginx
  320  docker ps
  321  curl 172.17.0.5
  322  curl 10.0.8.126
  323  curl 10.0.8.126:32768
  324  systemctl status docker
  331  docker run -d --name test-web-3 -p 8080:80  nginx
  332  docker ps
  333  docker run -d --name my-web-1 -p 8081:80 amitvashist7/docker-k8s-ey-we-25-cct-2025-apache:v4
  334  docker ps
  335  curl 10.0.8.126:32768
  336  curl 10.0.8.126:8080
  337  curl 10.0.8.126:8081
  338  netstat -tulnp
  339  netstat -tulnp | grep -i proxy
  340  systemctl status docker
  341  docker ps
  342  docker stop test-web-3
  343  netstat -tulnp | grep -i proxy
  344  systemctl status docker
  345  docker start test-web-3
  346  netstat -tulnp | grep -i proxy
  347  systemctl status docker
  348  docker stop test-web-3
  349  systemctl status docker
  350  docker run -itd ubuntu bash
  351  docker start test-web-3
  352  systemctl status docker
  353  curl 10.0.8.126:8080
```
