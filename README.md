# mysql 

-docker para lanzar un mysql en el puerto 3006

# serverMysqlAppNginx
     #preparado con 

     -php
     -composer
     -npm
     -node
     -mysql
     -nginx

## nuevo dev

     1º ir al archivo .env cambiar puertos locales de nginx y DB_LOCAL_ACCES

     2º entrar en docker-compose y cambiar los nombres de los servicios y de la red

     3º ir al archivo nginx app.conf y a la linea fastcgi_pass apptest:9000;
          y cambiar apptest por el nombre que le hayas puesto al primer servicio


## comandos

1ºcrear dockers

     docker-compose --env-file ../.env build "nombre del primer servicio"

     docker-compose --env-file ../.env build apptest

2ºlanzar dockers

     docker-compose --env-file ../.env  up -d 
