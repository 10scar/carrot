
# Carrot App

Backend en Laravel y Front en VueJS


## Authors

- [@10scar](https://github.com/10scar)


## Deployment

*Tener archivo env. por defecto usar env example

```bash
  docker-compose build app
```
```bash
  docker-compose up -d
```

puede revisar el estado con:
```bash
  docker-compose ps
```

## Installation
Su entorno ahora estárá configurado y en funcionamiento, pero aún debemos ejecutar algunos comandos para finalizar la configuración de la aplicación. Puede usar el comando docker-compose exec para ejecutar comandos en los contenedores de servicios, como ls -l. Este muestra información detallada sobre los archivos en el directorio de la aplicación:


```bash
  docker-compose exec app composer install
```

Lo último que debemos hacer antes de probar la aplicación es generar una clave de aplicación única con la herramienta de línea de comandos de Laravel artisan. Esta clave se utiliza para cifrar las sesiones de los usuarios y otros datos confidenciales:
```bash
  docker-compose exec app php artisan key:generate
```

* Si desea pausar su entorno de Docker Compose mientras mantiene el estado de todos sus servicios, ejecute lo siguiente:

 docker-compose pause


* Luego podrá reanudar sus servicios con lo siguiente:

  docker-compose unpause

* Para cerrar su entorno de Docker Compose y eliminar por completo sus contenedores, redes y volúmenes, ejecute lo siguiente:
```bash
  docker-compose down
```

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`API_KEY`


