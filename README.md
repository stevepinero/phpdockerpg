DOCKER COMPOSE PARA EJECUTAR PROYECTOS LARAVEL:
===============================================

**POR: STEVE PIÑERO**

Pasos para ejecutar:

1. copiar estos archivos en la raiz del proyecto laravel. 
2. configurar el .env con los parametros de conexion para la base de datos tomando en cuenta lo siguiente:<br>
    DB_CONNECTION=pgsql<br>
    DB_HOST=postgres<br>
    DB_PORT=5432<br>
    DB_DATABASE=db<br>
    DB_USERNAME=postgres<br>
    DB_PASSWORD=postgres<br>

    Donde DB_HOST es el nombre del contenedor dentro del docker-compose, al igual que el nombre de la base de datos y el usuario y clave del postgres. 
3. Luego ejecutar con el comando: `docker-compose up -d`
4. Para acceder a la consola del contenedor php ejecutar: <br> `docker-compose exec php-fpm bash` <br>
        **al ejecutar este comando tenemos la consola de php y en este momento se ejecuta los comandos compose y artisan.**