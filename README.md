# Template Docker para trabajo con PHP7 Nginx y Mariadb

## Preparar y Correr Contenedores:

```bash
$ docker-compose build
$ docker-compose up -d
```

## Comandos Útiles:

```bash
$ docker-compose stop
$ docker-compose ps

$ docker-compose exec db shell
$ docker-compose exec php shell
$ docker-compose exec nginx shell
```

## TODO

1. Solucionar problema al montar volumen de base de datos
