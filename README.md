# nCube-Lavender
## Introduction
The nCube:Lavender is an independent terminals, and as a separate device it can storage resources but cannot be take remoteCSE as child resource storage.It plays the role of ASN-CSE in the oneM2M standard. nCube:Lavender is a kind of nCube but it can active like server  because it contains CSE. The nCube:Lavender is same to Mobius on software level and they share the same type of oneM2M resource all most have same function. We can only use hardware environment to distinguish them.
## Connectivity stucture
<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28208839-b743eba2-68ca-11e7-9470-686193396ef6.png" width="600"/>
</div>

## Installation
The nCube:Lavander was developed with javascript of node.js and it also uses the MySQL to store data.
<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28209096-00fdcaa0-68cc-11e7-9d15-0a7dde6accb7.png" width="400"/>
</div><br/>

- [MySQL Server](https://www.mysql.com/downloads/)<br/>
The MySQL is an open source RDB database so that it is free and ligth. And RDB is very suitable for storing tree data just like oneM2M resource stucture. Most of nCube:Lavender will work in a restricted hardware environment and the MySQL can work in most of embeded devices.

- [Node.js](https://nodejs.org/en/)<br/>
Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world. Node.js is very powerful in service impelementation because it provide a rich and free web service API. So, we use it to make RESTful API base on the oneM2M standard.
- [nCube:Lavender](https://github.com/IoTKETI/nCube-Lavender/archive/master.zip)<br/>
nCube:Lavender is application base the node.js javascript. So we don't need to compile and install it before using.

## Configuration
- Import SQL script<br/>
When installation of MySQL Server finish. It also needs DB Schema for storing oneM2M resource in nCube:Lavender. You can find this file in the nCube:Lavender's source directory as below.
```
[nCube:Lavender home]/mobius/mobiusdb.sql
```
- Open the nCube:Lavender source home directory.
- Install dependency libraries with command like below.
```
npm install
```
- Modity configuration file "conf_mn.json"
<div align="left">
<img src="https://user-images.githubusercontent.com/29790334/28210356-ea6875aa-68d1-11e7-9023-00747a2d8597.png" width="300"/>
</div><br/>

## Running
Use node.js application execution command to run the Lavender
```
node lavender.js
```

<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28210479-9b4d0444-68d2-11e7-9502-77e47cb1da1c.png" width="700"/>
</div><br/>

## Dependency Libraries
These is dependency libraries for nCube:Lavender 
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
If you want more detail please dowload the full [installation guide document](https://github.com/IoTKETI/nCube-Lavender/raw/master/doc/Installation%20Guide_Lavender_v2.0.0_KR.docx).

# Author
Il Yeup (iyahn@keti.re.kr; ryeubi@gmail.com)
