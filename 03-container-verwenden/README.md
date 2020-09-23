# Folge 3: Container verwenden

- [Video der Folge 3: Container verwenden](https://www.youtube.com/watch?v=UxPm7IO9pP0)

In der dritten Folge wird der Umgang mit Containern geübt.

## Container "hello-world" starten

```shell
$ docker run hello-world
```

## Container interaktiv starten

```shell
$ docker run -it ubuntu
$ ...
$ exit
```

## Container auflisten

- Laufende Container auflisten
  ```shell
  $ docker ps
  ```

- Auch beendete Container auflisten
  ```shell
  $ docker ps -a
  ```

## Container im Hintergrund starten

```shell
$ docker run -d ubuntu sleep 30
```

## Container beenden

```shell
$ docker kill container_id
$ docker stop container_id
```

## Hostsystem aufräumen

- Alle beendeten Container löschen

```shell
$ docker container prune
```

- Nicht mehr benötigte Images löschen

```shell
$ docker image prune
```

- Ganzes Hostsystem aufräumen

```shell
$ docker system prune
```

## Portweiterleitung

```shell
$ docker run -d -p 8080:80 httpd
```

## Wichtige Links der Folge

- [Docker](https://docker.com)
- [Dokumentation Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Dokumentation zu Docker Desktop](https://docs.docker.com/desktop)
