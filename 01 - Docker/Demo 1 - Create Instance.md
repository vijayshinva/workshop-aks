docker run --name docker-one -p 8080:80 -d vijayshinva/dockerone

docker run --name aci-hello -p 8080:80 -d mcr.microsoft.com/azuredocs/aci-helloworld

docker run --name some-nginx -p 8080:80 -v C:/Delete/SimpleHtml:/usr/share/nginx/html:ro -d nginx

docker logs docker-one --follow

docker container exec -it docker-one /bin/bash

docker container exec -it docker-one curl bing.com

docker ps -a

docker stop docker-one

docker rm docker-one