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
more on [here](https://gist.github.com/stefanogarate/3355ff1a1702bca5d0b3fec74d8d9713)

## TODO

1. Solucionar problema al montar volumen de base de datos en windows (https://github.com/docker-library/mariadb/issues/95)
