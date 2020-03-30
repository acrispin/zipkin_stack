
# Docker version 19.03.5, build 633a0ea
docker --version

# docker-compose version 1.25.4, build 8d51620a
docker-compose --version

# para verificacion de contenedores
docker ps -a  
docker images  
docker network ls  

# se usa --compatibility por usar la key deploy en docker-compose.yml, es opcional, para que docker realize el limite de recursos
docker-compose --compatibility up -d  
docker-compose --compatibility up -d cassandra-service  
docker-compose --compatibility up -d rabbitmq-service  
docker-compose --compatibility up -d zipkin-service  

# reconstruye las imagenes
docker-compose --compatibility up -d --build

# detener, construir y ejecutar un servicio
docker-compose --compatibility stop zipkin-service  
docker-compose --compatibility build zipkin-service  
docker-compose --compatibility up -d zipkin-service  

# detener y eliminar todos los contenedores o servicios
docker-compose --compatibility down

# entrar al contener con bash o sh por servicio
docker-compose --compatibility exec cassandra-service sh  
docker-compose --compatibility exec rabbitmq-service sh  
docker-compose --compatibility exec zipkin-service bash  
docker-compose --compatibility exec curator sh  

# logs de los servicios
docker-compose logs -f cassandra-service  
docker-compose logs -f rabbitmq-service  
docker-compose logs -f zipkin-service  
docker-compose logs -f --tail 10  
docker-compose logs -f --tail 10  cassandra-service  

docker logs -f --tail 10 CONTAINER_NAME  
docker logs -f --tail 10 server-zipkin  

# Eliminar todas las imagenes
docker rmi $(docker images -aq)

# En linux rhel
## 1 Copiar carpeta con usuario root

## 2 Ingresar como usuario root

## 3 Ejecutar
docker-compose --compatibility up -d

## 4 Verificar 
docker ps  
docker stats

## 5 Verificar logs
docker-compose --compatibility logs  
docker-compose --compatibility logs -f cassandra-service  
docker-compose --compatibility logs -f rabbitmq-service  
docker-compose --compatibility logs -f zipkin-service  

## 6 Exponer el puerto 9411
firewall-cmd --zone=public --permanent --add-port=9411/tcp  
firewall-cmd --reload  
