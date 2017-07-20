# wsProject

This is a webrtc + websocket video call example.

* wsServer.js: a secured websocket server runnung on nodejs
* wsClient.html: a websocket client + webrtc client

I've host a public wsServer on:

   ***wss://signal.advancedrobotics.cc:1337***
   
You can immediately try the web app demo via chrome/firefox browser with the url:

   ***https://signal.advancedrobotics.cc/wsClient.html***

The public server is not guaranteed to be always on.

# Features

* Video call establish between two PCs
* Support chrome and firefox browser
* NAT & Firewal traversal based on STUN/TURN/ICE


# How to Use
## Install git on ec2 
    sudo yum install git

## clone this project
    git clone https://github.com/wennycooper/wsproject

## Install httpd with signed certificate (TOUGH job!!)

## copy client files into httpd folder
    cd ~wsproject
    cp wsClient.html /var/www/html
    cp adapter.js /var/www/html

## Install nodejs on ec2 standard AMI
    sudo yum install nodejs npm --enablerepo=epel


## Install websocket module
    cd wsProject
    npm install websocket
    
## Run wsServer
    node ./wsServer

## Run wsClient
    In PC1, open chrome/firefox browser and access https://YOUR_HTTPS_SERVER/wsClient.html
    In PC2, open chrome/firefox browser and access https://YOUR_HTTPS_SERVER/wsClient.html
    and on one PC, click [Call] button, the call should be established.



## ToDo

1. User registration process

# References

1. http://html5videoguide.net/presentations/WebDirCode2012/websocket/websocket-server.js
2. http://www.html5rocks.com/en/tutorials/webrtc/basics/
3. http://www.html5rocks.com/en/tutorials/webrtc/infrastructure/#beyond-browsers-voip-telephones-and-messaging
4. http://www.gtwang.org/2014/09/webrtc-media-stream.html
5. http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/SSL-on-an-instance.html

