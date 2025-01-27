---
id: overview
title: Overview
---

## General Description

In this section we will describe the current status and changes for a given release.

Be aware that some are as simple as changing version numbers while others need some extra configuration and some might even need some tweaking inside a docker container.

## Most recent versions

Below is the list of most recent versions split into own services and 3rd party components.

If you want to check what services/components need changes for a given release please see our [version history](../releases/versionhistory.md).

If you want to check the individual service/component please klick on the corresponding link.

### Own services
|Service|Current image version|
|--- |--- |
|[AgencyService](../releases/agencyservice.md)|`dockerImage.v.121.release-2021-03-02`|
|[Frontend](../releases/frontend.md)|`dockerImage.v.126-release-2021-03-23`|
|[LiveService](../releases/liveservice.md)|`dockerImage.v.14.release-2021-02-09`|
|[MailService](../releases/mailservice.md)|`dockerImage.v.13.release-2021-03-23`|
|[MessageService](../releases/messageservice.md)|`dockerImage.v.25.release-2021-03-23`|
|[NGINX](../releases/nginx.md)|`dockerImage.v.4.release-2020-11-03`|
|[UploadService](../releases/uploadservice.md)|`dockerImage.v.19.release-2021-03-02`|
|[UserService](../releases/userservice.md)|`dockerImage.v.78.release-2021-03-23`|
|[VideoService](../releases/videoservice.md)|`dockerImage.v.9.release-2021-02-08`|
 
### 3rd party components
|Component|Current image version|
|--- |--- |
|[Adminer](../releases/adminer.md)|`4.7.7`|
|[Keycloak](../releases/keycloak.md)|`11.0.2`|
|[MariaDB](../releases/mariadb.md)|`10.5.6`|
|[MongoDB](../releases/mongodb.md)|`4.0.5`|
|[Nosqlclient](../releases/nosqlclient.md)|`4.0.1`|
|[OpenLDAP](../releases/openldap.md)|`1.4.0`|
|[Rocket.Chat](../releases/rocketchat.md)|`3.7.1`|

 
### Backend stacks
To tie the services and components together we use a repository called ```backend```.\
For the VideoBeratung we have a dedicated backend: ```videoBackend```.

|Backend-Component|
|--- |
|[Backend](../releases/backend.md)|
|[VideoBackend](../releases/videobackend.md)|
