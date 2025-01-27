---
id: build-and-load-docker-image
title: Docker Image lokal bauen und in Docker laden
---
## AgencyService
### Docker-Image lokal bauen
Ein Docker-Image kann vom Service lokal mit folgendem Befehl bzw. dem Aufruf folgender Batchdatei, welche im Root-Verzeichnis des Service zu finden ist, gebaut werden:

`build-docker.cmd`

Das Image wird mit dem Tag `development` in der lokale Docker-Registry abgelegt und kann lokal für die Entwicklung verwendet werden.

### Docker-Image übertragen
Um das Docker-Image in einer andere Docker-Registry (z.B. anderer PC) zu übertragen können folgende Befehle verwendet werden:

**Export**
`docker save -o agencyservice.tar cob/agencyservice:development`

**Import**
`docker load -i agencyservice.tar`

## MailService
### Docker-Image lokal bauen
Ein Docker-Image kann vom Service lokal mit folgendem Befehl bzw. dem Aufruf folgender Batchdatei, welche im Root-Verzeichnis des Service zu finden ist, gebaut werden:

`build-docker.cmd`

Das Image wird mit dem Tag `development` in der lokale Docker-Registry abgelegt und kann lokal für die Entwicklung verwendet werden.

### Docker-Image übertragen
Um das Docker-Image in einer andere Docker-Registry (z.B. anderer PC) zu übertragen können folgende Befehle verwendet werden:

**Export**
`docker save -o mailservice.tar cob/mailservice:development`

**Import**
`docker load -i mailservice.tar`

## MessageService
### Docker-Image lokal bauen
Ein Docker-Image kann vom Service lokal mit folgendem Befehl bzw. dem Aufruf folgender Batchdatei, welche im Root-Verzeichnis des Service zu finden ist, gebaut werden:

`build-docker.cmd`

Das Image wird mit dem Tag `development` in der lokale Docker-Registry abgelegt und kann lokal für die Entwicklung verwendet werden.

### Docker-Image übertragen
Um das Docker-Image in einer andere Docker-Registry (z.B. anderer PC) zu übertragen können folgende Befehle verwendet werden:

**Export**
`docker save -o messageservice.tar cob/messageservice:development`

**Import**
`docker load -i messageservice.tar`

## UserService
### Docker-Image lokal bauen
Ein Docker-Image kann vom Service lokal mit folgendem Befehl bzw. dem Aufruf folgender Batchdatei, welche im Root-Verzeichnis des Service zu finden ist, gebaut werden:

`build-docker.cmd`

Das Image wird mit dem Tag `development` in der lokale Docker-Registry abgelegt und kann lokal für die Entwicklung verwendet werden.

### Docker-Image übertragen
Um das Docker-Image in einer andere Docker-Registry (z.B. anderer PC) zu übertragen können folgende Befehle verwendet werden:

**Export**
`docker save -o userservice.tar cob/userservice:development`

**Import**
`docker load -i userservice.tar`

## UploadService
### Docker-Image lokal bauen
Ein Docker-Image kann vom Service lokal mit folgendem Befehl bzw. dem Aufruf folgender Batchdatei, welche im Root-Verzeichnis des Service zu finden ist, gebaut werden:

`build-docker.cmd`

Das Image wird mit dem Tag `development` in der lokale Docker-Registry abgelegt und kann lokal für die Entwicklung verwendet werden.

### Docker-Image übertragen
Um das Docker-Image in einer andere Docker-Registry (z.B. anderer PC) zu übertragen können folgende Befehle verwendet werden:

**Export**
`docker save -o uploadservice.tar cob/uploadservice:development`

**Import**
`docker load -i uploadservice.tar`

## LiveService
### Docker-Image lokal bauen
Ein Docker-Image kann vom Service lokal mit folgendem Befehl bzw. dem Aufruf folgender Batchdatei, welche im Root-Verzeichnis des Service zu finden ist, gebaut werden:

`build-docker.cmd`

Das Image wird mit dem Tag `development` in der lokale Docker-Registry abgelegt und kann lokal für die Entwicklung verwendet werden.

### Docker-Image übertragen
Um das Docker-Image in einer andere Docker-Registry (z.B. anderer PC) zu übertragen können folgende Befehle verwendet werden:

**Export**
`docker save -o liveservice.tar cob/liveservice:development`

**Import**
`docker load -i liveservice.tar`

## VideoService
### Build docker image locally
You can build the Docker image of the VideoService with the following batch file which is located in the root directory:

`build-docker.cmd`

The image is being tagged as `development` in the local Docker registry. You may need to change the path in the `Dockerfile` for a correct build to (for example):

`COPY target/VideoService.jar app.jar`

### Transfer Docker image
To transfer the Docker image to another Docker registry (or another computer) you can use the following commands:

**Export**
`docker save -o videoservice.tar cob/videoservice:development`

**Import**
`docker load -i videoservice.tar`