# Labs-docker-dev

## Pulling an image

### imagen oficial de Ubuntu:

Using default tag: latest
latest: Pulling from library/ubuntu
9c704ecd0c69: Pull complete 
Digest: sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
Status: Downloaded newer image for ubuntu:latest
docker.io/library/ubuntu:latest

### Descarga de una versión específica de Python: 

3.9: Pulling from library/python
ca4e5d672725: Pull complete 
30b93c12a9c9: Pull complete 
10d643a5fa82: Pull complete 
d6dc1019d793: Pull complete 
c387064957b7: Pull complete 
26766ebde481: Pull complete 
8a42d17fd0e2: Pull complete 
79eda865cc8a: Pull complete 
Digest: sha256:fea84f3a3b72c41efe7fc3b07ae209c6856b852b942c05fa88b747b74f70e711
Status: Downloaded newer image for python:3.9
docker.io/library/python:3.9

## Running our container

### Contenedor de Ubuntu en modo interactivo: 

root@f432ef7ae156:/#

### Ejecutar un servidor web Apache en segundo plano:

docker run -d -p 8080:80 httpd 
Unable to find image 'httpd:latest' locally
latest: Pulling from library/httpd
efc2b5ad9eec: Already exists 
fce1785eb819: Pull complete 
4f4fb700ef54: Pull complete 
f214daa0692f: Pull complete 
05383fd8b2b3: Pull complete 
88ad12232aa1: Pull complete 
Digest: sha256:932ac36fabe1d2103ed3edbe66224ed2afe0041b317bcdb6f5d9be63594f0030
Status: Downloaded newer image for httpd:latest
16d7939d022282e17124461c1ceb2b48d70c0dad1e4cc497e142688069b14cab

## Removing containers

### Eliminar  el contenedor de Ubuntu:

docker rm f432ef7ae156
f432ef7ae156.


### Eliminar todos los contenedores detenidos:

docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Total reclaimed space: 0B


## Dockerfile básico: ubuntu

[+] Building 10.2s (6/6) FINISHED                                                                                      docker:default
 => [internal] load build definition from Dockerfile                                                                             0.3s
 => => transferring dockerfile: 96B                                                                                              0.0s
 => [internal] load metadata for docker.io/library/ubuntu:latest                                                                 0.0s
 => [internal] load .dockerignore                                                                                                0.2s
 => => transferring context: 2B                                                                                                  0.0s
 => [1/2] FROM docker.io/library/ubuntu:latest                                                                                   0.1s
 => [2/2] RUN apt-get update && apt-get upgrade -y                                                                               7.9s
 => exporting to image                                                                                                           1.3s
 => => exporting layers                                                                                                          1.2s
 => => writing image sha256:f0270fe971171fbdd8f17430011010ce8c7d16d74d262e439a2ff4369f34e851                                     0.0s
 => => naming to docker.io/library/ubuntu-updated:latest  

 ## Dockerfile: Nginx

 [+] Building 18.2s (6/6) FINISHED                                                                                      docker:default
 => [internal] load build definition from Dockerfile                                                                             0.8s
 => => transferring dockerfile: 138B                                                                                             0.0s
 => [internal] load metadata for docker.io/library/ubuntu:latest                                                                 0.0s
 => [internal] load .dockerignore                                                                                                0.1s
 => => transferring context: 2B                                                                                                  0.0s
 => CACHED [1/2] FROM docker.io/library/ubuntu:latest                                                                            0.0s
 => [2/2] RUN apt-get update && apt-get install -y nginx                                                                        16.4s
 => exporting to image                                                                                                           0.5s
 => => exporting layers                                                                                                          0.4s
 => => writing image sha256:afcda046831326b2781430b8e30879f47ab0795345fd3999ea048043d45c53fa                                     0.0s
 => => naming to docker.io/library/ubuntu-updated:latest 

## Ejecutar imagen

0760e3abc04e3ac622589aa0d749a84056ab8bd4fc0c14fc0a19adbf5b2a2968


