# PHP 8.2 y Postgresql

## DOCKER COMPOSE PARA EJECUTAR PROYECTOS LARAVEL:
===============================================

### POR: STEVE PIÑERO

Pasos para ejecutar:

1. copiar estos archivos en la raiz del proyecto laravel. 
2. configurar el .env con los parametros de conexion para la base de datos tomando en cuenta lo siguiente:

    ```text
    DB_CONNECTION=pgsql
    DB_HOST=postgres
    DB_PORT=5432
    DB_DATABASE=db
    DB_USERNAME=postgres
    DB_PASSWORD=postgres
    ```

    Donde DB_HOST es el nombre del contenedor dentro del docker-compose, al igual que el nombre de la base de datos y el usuario y clave del postgres.
3. Luego ejecutar con el comando:

    ```text
    docker-compose up -d
    ```

4. Para acceder a la consola del contenedor php ejecutar:

    ```text
    docker-compose exec php-fpm bash
    ```

    **al ejecutar este comando tenemos la consola de php y en este momento se ejecuta los comandos compose y artisan.**