# environment-docker
Docker PHP 5.6/7.1 Nginx

### Instructions

````sh
# install ubuntu in docker - ubuntu:latest
docker pull ubuntu

# build image to webserver 7.1/nginx
sudo docker build -t webserver .

# build image to webserver 5.6/nginx
cd php56/
sudo docker build -t webserver56 .

# up nginx with php 7.1
docker run -it --name nginxphp71 -d -p 8088:80 webserver:latest

# up nginx with php 5.6
docker run -it --name nginxphp56 -d -p 8098:80 webserver56:latest
````