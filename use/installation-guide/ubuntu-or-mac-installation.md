---
description: >-
  Installation steps for coKreat reference web app on Unix (Ubuntu or Mac)
  environment
---

# Ubuntu or Mac Installation

### Pre - required programs

* Python 2.7.18&#x20;

[Note : If your machine has python 3+ installed, please downgrade it to 2.7](#user-content-fn-1)[^1]

### Follow-up steps&#x20;

* Install node version 14.18.1&#x20;
* Install Angular CLI: 13.3.3&#x20;
* Create git account&#x20;
* Clone the repo from : https://github.com/Sunbird-Ed/creation-portal.git

[Note : ](#user-content-fn-2)[^2]Clone the repo to desktop folder to avoid any privileged user access problems

### Run the application server&#x20;

* Open terminal
* Change directory to ..\creation-portal\src\app
* Run command `set NODE_OPTIONS=--max_old_space_size=4096`&#x20;
* Run command `npm i`&#x20;
* Run command `npm run resource-bundles`&#x20;
* Run command `export sunbird_environment="local"`&#x20;
* Run command `export sunbird_instance="sunbird"`&#x20;
* Run command `export sunbird_default_channel="sunbird"`&#x20;
* Run command `export sunbird_default_tenant="sunbird"`&#x20;
* Run command `node server`

### Run the client&#x20;

* Open another command prompt window&#x20;
* Change directory to ..\creation-portal\src\app\client&#x20;
* Run command `npm i`
* Run command `npm install nodemon`&#x20;
* Run command `nodemon`&#x20;

Open `http://localhost:3000/sourcing` on a browser tab

[^1]: 

[^2]: 
