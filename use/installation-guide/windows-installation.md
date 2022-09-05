---
description: Installation steps for coKreat reference web app on Windows environment
---

# Windows Installation

### Pre - required programs

Python 2.7.18 Visual studio build tools 2017 (v15.9)

C++/cli support) build tools core features windows 10 sdk c++/cli support

### Follow-up steps&#x20;

Install node version 14.18.1&#x20;

Install Angular CLI: 13.3.3&#x20;

Create git account&#x20;

Clone the repo from : https://github.com/Sunbird-Ed/creation-portal.git

### Run the application server&#x20;

Open command prompt&#x20;

Change directory to ..\creation-portal\src\app

`set NODE_OPTIONS=--max_old_space_size=4096`&#x20;

`npm i`&#x20;

`npm run resource-bundles`&#x20;

`set sunbird_environment="local"`&#x20;

`set sunbird_instance="sunbird"`&#x20;

`set sunbird_default_channel="sunbird"`&#x20;

`set sunbird_default_tenant="sunbird"`&#x20;

`node server`

### Run the client&#x20;

Open another command prompt window&#x20;

Change directory to ..\creation-portal\src\app\client&#x20;

Change `mv` command in `package.json` to `move` command

`npm i`

`npm install nodemon`&#x20;

Run command `nodemon`&#x20;

Open `http://localhost:3000/sourcing` on a browser tab
