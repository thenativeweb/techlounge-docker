# Folge 4: Images bauen

- [Video der Folge 4: Images bauen](https://www.thenativeweb.io/learning/techlounge-docker)

In der vierten Folge wird das erste eigene Image gebaut.

## Workspace erstellen

Beispiel-Applikation mit Express erstellen.

```shell
$ mkdir hello
$ cd hello
```

## Express-Applikation erstellen

Die Beispiel-Applikation mit `npx` und dem Express-Generator erstellen:

```shell
$ npx express-generator
```

Alternativ mit Docker erstellen:

```shell
$ docker run -v "$(pwd):/hello" -w /hello node:lts-alpine npx express-generator
```

## Dockerfile

```dockerfile
FROM node:lts-alpine
WORKDIR /app
COPY package.json .
RUN npm install
COPY . .
EXPOSE 3000
CMD [ "npm", "start" ]
```

## Image bauen

```shell
$ docker build -t hello .
```

## Applikation starten

```shell
$ docker run -d -p 8080:3000 hello
```

Im Browser öffnen: http://localhost:8080

## Eigenes Image auf den Docker Hub

```shell
$ docker tag hello dockerid/hello
$ docker push dockerid/hello
```

## Wichtige Links der Folge

- [Offizielles Node.js-Image](https://hub.docker.com/_/node)
- [Docker](https://docker.com)
- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Dokumentation zu Docker Desktop](https://docs.docker.com/desktop)
- [Dokumentation der VSCode Docker Extension](https://code.visualstudio.com/docs/containers/overview)
