# PHP 8.2 y Postgresql

## DOCKER COMPOSE PARA EJECUTAR PROYECTOS LARAVEL

### POR: STEVE PIÑERO

---
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

## **Docker compose cheatsheet**

**Note:** debe estar dentro de la carpeta donde este el archivo docker-compose.yml porque sino no funcionará.

* Ejecutar los contenedores en background:
    `docker-compose up -d`
* Ver los logs de los contenedores: `docker-compose logs`
* Ejecutar contenedores en pantalla, también veran los logs de los contenedores que estén corriendo (si cierra la ventana se apagarán):
    `docker-compose up`
* Detener contenedores: `docker-compose stop`
* Matar los procesos de los contenedores: `docker-compose kill`
* Parar y borrar todos los contenedores: `docker-compose down`
* Ejecutar comandos dentro de un contenedor: `docker-compose exec SERVICE_NAME COMMAND` donde `COMMAND` es el comando a ejecutar. **Por ejemplo**:
  * Ejecutar bash dentro del contenedor PHP, `docker-compose exec php-fpm bash`
        **al ejecutar este comando tenemos la consola de php y en este momento se ejecuta los comandos compose y artisan.**
  * Abrir la consola de Mysql, `docker-compose exec mysql mysql -uroot -pCHOSEN_ROOT_PASSWORD`

