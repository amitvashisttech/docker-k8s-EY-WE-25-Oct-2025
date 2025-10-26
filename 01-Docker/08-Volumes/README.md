
## Static Volume
```
  346  docker ps
  347  docker volume ls
  348  docker volume create myvol1
  349  docker volume ls
  350  docker volume inspect myvol1
  351  ls -ltr /var/lib/docker/volumes/myvol1/_data/
  352  ls
  353  docker run -it stg-1 -v myvol1:/myapp ubuntu
  354  docker run -it --name stg-1 -v myvol1:/myapp ubuntu
  355  docker ps
  356  docker inspect stg-1
  357  cat /var/lib/docker/volumes/myvol1/_data/hello.txt
  358  docker run -it --name stg-2 -v myvol1:/var/www/html ubuntu
  359  docker ps
  360  docker run -it --name stg-3 -v myvol1:/amit:ro ubuntu
```

## Dynamic Volume 
```
  369  docker run -it --name stg-dynamic-1 -v /myvol1 ubuntu
  370  docker ps
  371  docker inspect stg-dynamic-1
  372  docker volume ls
  373  cat /var/lib/docker/volumes/a42fc8849ff0ab7466fc4bc8282e03de1a6eaf29fa853d006e0abcc021e4e70b/_data/info
  374  docker run -it --name stg-dynamic-2 -v /myvol1 -v /amit -v /ey -v /dockervoldemo ubuntu
  375  docker volume ls
  376  docker ps
  377  docker inspect stg-dynamic-2
  378  cat /var/lib/docker/volumes/bf6a992ac5b29d1f86662cb774bfc9ebc9ec3b041d577efb6ebc60243c671742/_data/abc.txt
```

## Dir Mapping / Binding 
```
  383  docker run -it --name stg-dir-map-1 -v /root/docker-k8s-EY-E-02-Dec-2024:/myvol1  ubuntu
  384  ls
  385  cat hello.txt
  386  docker run -it --name stg-dir-map-2 -v /root/docker-k8s-EY-E-02-Dec-2024:/myvol1:ro  ubuntu
  387  docker volume ls
  388  docker ps
  389  docker inspect stg-dir-map-1
  390  docker start stg-dir-map-2
  391  docker ps
  392  docker inspect stg-dir-map-2
```
