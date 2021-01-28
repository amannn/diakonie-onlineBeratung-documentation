---
id: video-backend
title: Installing and running the videoBackend
---

In this page we will show how to configure and start a videoBackend.

## Prerequisites
You need some of the same prerequisites as for the [backend](../backend/install-and-running-locally.md):
 - docker-compose
 - a url like ```onlineberatung.local``` or ```onlineberatung.de```
 - your local IP address (for local usage)
 
## Steps
 
### Get the files
You have two ways to get the files:
 - checkout with git
 - download as a zip-file

For both ways you need to go to the [videoBackend GitHub Repository](https://github.com/CaritasDeutschland/caritas-onlineBeratung-videoBackend)

### Create the .env (configuration)
To make our lives easier there is a sample file ```.env.sample```

Copy or rename this file to ```.env```. After that you can customize the file for your needs i.e. :
 - Passwords
 - Ports
 - URL
 - Local IP (for local usage)

### Generate passwords
Generally speaking: we need strong passwords everywhere

The Jitsi Community knows that and therefore created a script to support us in that task: ```gen-passwords.sh```

So just run this file in the directory with the ```.env``` file if you can.

After that check the ```.env``` file to make sure all 6 password variables are set:
 - ```JICOFO_COMPONENT_SECRET```
 - ```JICOFO_AUTH_PASSWORD```
 - ```JVB_AUTH_PASSWORD```
 - ```JIGASI_XMPP_PASSWORD```
 - ```JIBRI_RECORDER_PASSWORD```
 - ```JIBRI_XMPP_PASSWORD```

Alternatively: \
Create passwords of your own (i.e. with a Password Manager) and update the above mentioned variables yourself.

### Change ports (if necessary)
There are two ports configured in ```.env```:
 - ```HTTP_PORT``` for HTTP traffic (insecure)
 - ```HTTPS_PORT```  for HTTPS traffic (secure)

For local usage you don´t need to change the default ports. 

If you want to use the videoBackend outside of your local machine you might want to change the ports to 
 - 80 for ```HTTP_PORT```
 - 443 for ```HTTPS_PORT```

### Update URL
You need to configure a URL where your videoBackend is reachable at ```PUBLIC_URL``` in ```.env```.

For local development you can re-use the URL from the backend ```onlineberatung.local``` with the default ports.

ℹ You need to ensure that this URL points to the machine where you intent to start the videoBackend.
 - for ```onlineberatung.local``` you might need to edit your ```hosts``` file and add ```onlineberatung.local``` pointing to ```127.0.0.1``` or the ```ip-address``` of your machine.
 - for ```onlineberatung.de``` (or your Domain) you need to add a DNS record pointing to the ```ip-address``` of the machine running the videoBackend.

### Set DOCKER_HOST_ADDRESS
If you run your videoBackend on a local machine or behind a NAT (i.e. with forwarded ports) you need to put your IP at ```DOCKER_HOST_ADDRESS``` in ```.env``` and uncomment that specific line by removing the leading ```#```.
 - for your local Machine this needs to be your IP address (not 127.0.0.1)
 - for a server behind a NAT, this needs to be the external IP address

## videoBackend startup
After you configured your videoBackend you can start it by running the command ```docker-compose up -d``` in the directory containing the ```.env``` and ```docker-compose.yml``` files.
 
## Known difficulties
 
### Self-Signed Certificate with Chrome
If you can't access the Jitsi page because of a warning about an invalid certificate in Chrome, you can try this tip:\
Just click anywhere on the screen (to select the tab/page) and type ```thisisunsafe```

This is especially true for Chrome on Mac since it treats things different as the Windows version.

See [Stackoverflow](https://stackoverflow.com/questions/58802767/no-proceed-anyway-option-on-neterr-cert-invalid-in-chrome-on-macos/58957322#58957322)
 
 