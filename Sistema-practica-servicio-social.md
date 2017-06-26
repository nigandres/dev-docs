# Aasistencias de servicio social

## Crear nuevo proyecto de Laravel

`laravel new nombre_proyecto`

Verificar si el proyecto es accesible desde navegador:
http://nombre_proyecto

## Crear base de datos

- Ingresar a mysql 
- `create database nombre_base_de_datos`

## Configurar archivo .env

- Configurar nombre de la base de datos

## Creación de tablas para usarios y carreras

### Usuarios

- Utilizar `php artisan make:auth`
- Modificar migración (database/migrations/*_create_users_table.php) para que contenga:
    - id
    - nombre
    - correo
    - pasword
    - codigo
    - rol
    - carrera_id
    - Utilizar rememberToken() y timestamps()

### Carreras

- Crear modelo controlador y migración para "carreras" utilizando `php artisan make:model -mcr Carrera`
- Modificar migración *_create_carreras_table.php para que contenga:
    - id
    - carrera
- Modificar modelo Carrera (app/Carrera.php)
    - Agregar `public $timestamps = false;`
    - Agregar `protected $fillable = ['carrera];`


## Referencias

[Repositiorio de proyecto en GitHub](https://github.com/samuelmg/social)




