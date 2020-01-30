# Akọ̀wé

Akọ̀wé (Yoruba word for a clerk) is a serverless version of [Kotype](https://github.com/webodf/Kotype), a web-based collaborative real-time editing server for OpenDocuments.
Akọ̀wé uses static web pages hosted here on Github and does not require any server-side code to be installed and configured to work. 

Instead, Akọ̀we uses a standard public XMPP server extended with [Colibri](https://xmpp.org/extensions/xep-0340.html) like [Jitsi-Meet](https://meet.jit.si) or [Openfire Meetings](https://github.com/igniterealtime/openfire-ofmeet-plugin) together with standard XMPP Multi-User Chat (MUC) to provide conferencing and routing of messages betweeen all collaborating editors.

## Demo
Open two browser window/tabs instances and point them at https://inspired-futures.github.io/akowe/?audio=true

## Installation
Nothing to install!. It is is serverless. Just clone this GitHub repository and enabled GitPages for the docs folder. 

## How to use
First edit index.js and change the default settings in kotypeGlobals. Next, open two browser window/tabs instances and point them at the github.io URL of your clone.

To make full use of Akọ̀wé, you should embed it in your own application with an <iframe> and provide the required settings with parameters in the URL. The full list of parameters that can be used are as follows:


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





