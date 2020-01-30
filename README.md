# Akọ̀wé

Akọ̀wé (Yoruba word for a clerk) is a serverless version of [Kotype](https://github.com/webodf/Kotype), a web-based collaborative real-time editing server for [OpenDocuments](https://en.wikipedia.org/wiki/OpenDocument) (an open, XML-based file format specification for office applications) using [XMPP](https://en.wikipedia.org/wiki/XMPP) (a communication protocol for message-oriented middleware based on XML).

Akọ̀wé uses static web pages hosted here on Github or any basic web server and does not require any server-side code to be installed and configured to work. No PHP, no Java, no NodeJS, just serveless with plain HTML, CSS and JavaScript!!.

Akọ̀we requires a standard public XMPP server extended with [Colibri](https://xmpp.org/extensions/xep-0340.html) like [Jitsi-Meet](https://meet.jit.si) or [Openfire Meetings](https://github.com/igniterealtime/openfire-ofmeet-plugin) together with standard XMPP Multi-User Chat (MUC) to provide audio conferencing and service the collaborative editing of text documents.

<img src="https://inspired-futures.github.io/akowe/screenshot.png" />

## Demo
Open two browser window/tabs instances and point them at https://inspired-futures.github.io/akowe/?audio=true

## Installation
Nothing to install!. It is is serverless. Just clone this GitHub repository and enabled GitPages for the docs folder. 

## How to use
First edit index.js and change the default settings in kotypeGlobals. Next, open two browser window/tabs instances and point them at the github.io URL of your clone.

To make full use of Akọ̀wé, you should embed it in your own application with an <iframe> and provide the required settings with parameters in the URL. 
  
For example, this is an example URL that uses my gravatar public profile as shown above

https://inspired-futures.github.io/akowe/?audio=true&username=dele&name=Dele%20Olajide&avatar=https://secure.gravatar.com/avatar/3f633b302d459da237f35b47fd89a7eb

The full list of parameters that can be used is shown below:

| Parameter     | Default                          | Description                                |
|---------------|----------------------------------|--------------------------------------------|
| audio         | false                            | Audio Conferencing enabled                 |
| avatar        | unknown                          | image uri for user avatar (data:xxx)       |
| username      | unknown                          | An identifier for the user                 |
| name          | Unknown                          | The fullname or nickname of user           |
| docname       | welcome.odt                      | The genesis document for the collaboration |
| docurl        | ./welcome.odt                    | The url of the document to be edited       |
| domain        | meet.jit.si                      | XMPP domain                                |
| bosh          | wss://meet.jit.si/xmpp-websocket | XMPP server connection url                 |
| pwd           | undefined                        | XMPP user password for authentication      |
