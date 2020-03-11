
# Docker version 19.03.5, build 633a0ea
docker --version

# docker-compose version 1.25.4, build 8d51620a
docker-compose --version

docker ps -a
docker images
docker network ls

# se usa --compatibility por usar la key deploy en docker-compose.yml, es opcional, para que docker realize el limite de recursos
docker-compose --compatibility up -d
docker-compose --compatibility up -d microservicios-rabbitmq38
docker-compose --compatibility up -d elasticsearch6
docker-compose --compatibility up -d zipkin-server

# reconstruye las imagenes
docker-compose --compatibility up -d --build

# detener, construir y ejecutar un servicio
docker-compose --compatibility stop curator
docker-compose --compatibility build curator
docker-compose --compatibility up -d curator

# detener y eliminar todos los contenedores o servicios
docker-compose --compatibility down

# entrar al contener con bash o sh por servicio
docker-compose --compatibility exec microservicios-rabbitmq38 sh
docker-compose --compatibility exec elasticsearch6 sh
docker-compose --compatibility exec zipkin-server bas
docker-compose --compatibility exec curator sh

# logs de los servicios
docker-compose logs -f microservicios-rabbitmq38
docker-compose logs -f elasticsearch6
docker-compose logs -f zipkin-server

# Eliminar todas las imagenes
docker rmi $(docker images -aq)
