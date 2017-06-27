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

## Crear Seeder para tabla carreras

Laravel incluye un método para agregar registros (seeding) a las tablas usando la clase "seed" (semilla).

- Crear seeder: `php artisan make:seeder CarrerasTableSeeder` con lo que se creará el archivo: database/seeds/CarrerasTableSeeder.php
- Agregar 5 carreras utilizando el seeder. [Documentación para escribir Seeders](https://laravel.com/docs/5.4/seeding#writing-seeders)
- Una vez creado el seeder, ejecutar: `composer dump-autoload`
- Ejecutar seeder: `php artisan db:seed --class=CarrerasTableSeeder`
- Verificar si las carreras se agregaron a la tabla carreras

## Código fuente

[Repositiorio de proyecto en GitHub](https://github.com/samuelmg/social)




