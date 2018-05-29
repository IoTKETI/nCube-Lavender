# &Cube-Lavender
## Introduction
The &Cube-Lavender is the open source IoT device platform based on the oneM2M (http://www.oneM2M.org) standard. As one of the oneM2M platforms, &Cube-Lavender provides common services functions to oneM2M device applications that runs on the same device.

## Version
2.4.0

## Connectivity stucture
&Cube-Lavender implementation of oneM2M ASN-CSE which can be connected to MN-CSE or IN-CSE.
<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28208839-b743eba2-68ca-11e7-9470-686193396ef6.png" width="600"/>
</div>

## Installation
The &Cube-Lavender was developed with javascript of node.js and it also uses the MySQL to store data.
<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28209096-00fdcaa0-68cc-11e7-9d15-0a7dde6accb7.png" width="400"/>
</div><br/>

- [MySQL Server](https://www.mysql.com/downloads/)<br/>
The MySQL is an open source RDB database so that it is free and ligth. And RDB is very suitable for storing tree data just like oneM2M resource stucture. Most of &Cube-Lavender will work in a restricted hardware environment and the MySQL can work in most of embeded devices.

- [Node.js](https://nodejs.org/en/)<br/>
Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world. Node.js is very powerful in service impelementation because it provide a rich and free web service API. So, we use it to make RESTful API base on the oneM2M standard.
- [&Cube-Lavender](https://github.com/IoTKETI/nCube-Lavender/archive/master.zip)<br/>
&Cube-Lavender source codes are written in javascript. So they don't need any compilation or installation before running.

## Configuration
- Import SQL script<br/>
After installation of MySQL server, you need the DB Schema for storing oneM2M resources in &Cube-Lavender. You can find this file in the following &Cube-Lavender source directory.
```
[nCube-Lavender home]/mobius/mobiusdb.sql
```
- Open the &Cube-Lavender source home directory
- Install dependent libraries as below
```
npm install
```
- Modify configuration file "conf_asn.json" per your setting
```
{
  "parent": {
    "cbname": "Mobius",             //CSEbase name
    "cbcseid": "/Mobius",           //CSEbase ID
    "cbhost": "203.253.128.161",    //CSEbase host IP
    "cbhostport": "7579",           //CSEbase http hosting port
    "cbprotocol": "http",           //CSEbase communication protocol
    "mqttbroker": "203.253.128.161" //MQTT Broker IP 
  },
  "csebaseport": "7499",            //MN-CSE HTTP hosting IP
  "dbpass": "dksklfdug2"            //Local MySQL root password
}
```

## Running
Use node.js application execution command as below
```
node lavender.js
```

<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28210479-9b4d0444-68d2-11e7-9502-77e47cb1da1c.png" width="700"/>
</div><br/>

## Dependency Libraries
This is the list of library dependencies for &Cube-Lavender 
- body-parser
- cbor
- coap
- crypto
- events
- express
- file-stream-rotator
- fs
- http
- https
- ip
- js2xmlparser
- merge
- morgan
- mqtt
- mysql
- shortid
- url
- util
- websocket
- xml2js
- xmlbuilder

## Document
If you want more details please dowload the full [installation guide document](https://github.com/IoTKETI/nCube-Lavender/raw/master/doc/Installation%20Guide_Lavender_v2.0.0_KR.docx).

# Author
Il Yeup (iyahn@keti.re.kr; ryeubi@gmail.com)
