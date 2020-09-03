# Folge 1: Grundkonzepte

- [Video der Folge 1: Grundkonzepte](https://www.youtube.com/watch?v=e1BOFzxgQQY)

In der ersten Folge wird dieses [`Dockerfile`](./Dockerfile) gezeigt, um Dir den groben Aufbau zu zeigen.
Damit wird ein Apache 2 Image erstellt mit der Standardwebseite. Es dient auch zum Ausprobieren der ersten Befehle mit dem Docker-CLI.

## Image bauen

```shell
$ docker build -t apache2 .
```

- Die Option `-t` oder `--tag` vergibt einen Namen für das Image
- Der Punkt `.` am Ende bedeutet den Build-Kontext, üblicherweise dort, wo das Dockerfile liegt

## Container starten

```shell
$ docker run -d -p 8080:80 apache2
```

- Die Option `-d` oder `--detach` startet den Container im Hintergrund
- Die Option `-p` oder `--publish` verbindet ein Container-Port am Host

## Hochladen zum Docker Hub

```shell
$ docker login
$ docker tag apache2 dockerid/apache2
$ docker push dockerid/apache2
```

Tausche `dockerid` durch Deinen eigenen Namen auf dem Docker Hub.

## Herunterladen vom Docker Hub

```shell
$ docker login
$ docker pull dockerid/apache2
```

Tausche `dockerid` durch Deinen eigenen Namen auf dem Docker Hub.

## Weiter Schritte

Wie im Video erklärt, muss Du nicht von Null anfangen.

Um wirklich den Apache Webserver in einem Container zu nutzen, verwende das offizielle Image [`httpd`](https://hub.docker.com/_/httpd) vom Docker Hub. Dort wird auch die Verwendung beschrieben und wie man zum Beispiel die Standardwebseite mit eigenen Dateien austauscht.

## Wichtige Links der Folge

- [Docker](https://docker.com)
- [Docker Hub](https://hub.docker.com)
- [Play with Docker](https://docker.com/play-with-docker)
