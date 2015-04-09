# wsProject

This is a webrtc + websocket video call example.

* wsServer.js: a websocket server runnung on nodejs
* wsClient.html: a websocket client + webrtc client

I've put a public wsServer on "ws://ec2-54-149-233-189.us-west-2.compute.amazonaws.com/wsClient.html:1337"  
You can immediately try it using chrome browser with following url:

   ***http://ec2-54-149-233-189.us-west-2.compute.amazonaws.com/wsClient.html/wsClient.html***

It is not guaranteed to be always on.

# Features

* Video call establish between two PCs
* Support chrome and firefox browser
* NAT & Firewal traversal based on STUN/TURN/ICE


# How to Use
## Install git on ec2 
    sudo yum install git

## clone this project
    git clone https://github.com/wennycooper/wsproject

## Install nodejs on ec2
    sudo yum install nodejs npm --enablerepo=epel

## Install websocket module
    cd wsProject
    npm install websocket
    
## Run wsServer
    node ./wsServer

## Run wsClient
    In PC1, open chrome/firefox browser with wsClient.html
    In PC2, open chrome/firefox browser with wsClient.html, and click [Send Message] button, the video call should be established.

## ToDo

1. User registration process

# References

1. http://html5videoguide.net/presentations/WebDirCode2012/websocket/websocket-server.js
2. http://www.html5rocks.com/en/tutorials/webrtc/basics/
3. http://www.html5rocks.com/en/tutorials/webrtc/infrastructure/#beyond-browsers-voip-telephones-and-messaging
4. http://www.gtwang.org/2014/09/webrtc-media-stream.html

