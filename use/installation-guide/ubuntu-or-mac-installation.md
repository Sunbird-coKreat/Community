---
description: >-
  Installation steps for coKreat reference web app on Unix (Ubuntu or Mac)
  environment
---

# Ubuntu or Mac Installation

**Pre-Required Setup**\


* **System Requirements**
  * OS -> This document is for Installing CoKreate on an Ubuntu, linux and Mac Machines only, In case you are an Windows Operator please refer here\\
  * RAM should be 8 GB or Above
  * SSD/HDD more than 256 GB
*   **System Installations**

    Angular 14 or above

    Node 14.\
    (In case your machine is pointing to any other version please Install NVM and switch to Node 14)

    Python 2.7\
    (In case your machine is having any lower or higher version of python, Please install python 2.7 and mark it as default, Instructions are given here)

    Github Account to fork and clone the repository&#x20;

    Clone CoKreate repository from here https://github.com/Sunbird-coKreat/creation-portal

\


Notes: This Project will be configured in two terminals\
Terminal 1 -> To configure the server on your local machines\
Terminal 2 -> To configure the client on your local machine

IMP: Please do not change or alter any on the versions given above

\


* **Terminal 1 Setup**
  * Clone the Repo from GitHub [https://github.com/Sunbird-coKreat/creation-portal](https://github.com/Sunbird-coKreat/creation-portal)
  * Go to the cloned folder “cd creation-portal”
  * Change the folder by typing “cd src/app”
  * Execute the following commands
    * Set NODE\_OPTIONS=--max\_old\_space\_size=4096 (this will remove heap command)
    * Npm install (after NPM Install is done execute the below commands)
    * npm resource-bundles
  *   Once the above commands are successfully executed set System Variables

      export sunbird\_environment="local"

      export sunbird\_instance="sunbird"

      export sunbird\_default\_channel="sunbird"

      export sunbird\_default\_tenant="sunbird"
* Now do the client setup, Minimise this terminal and open new terminal or terminal tab
* After part 2 is done, set environment tokens and run the project\
  “**npm run server**”



* **Terminal 2 Setup:**
  * Point this terminal to cloned repo folder and go to client folder “cd src/app/client”
  *   Now run following commands

      **Npm install**
  * Now try running the client terminal “ng build –watch=true”
  * Now go to server terminal and run the “npm run server ”
  * This is setup creation portal on local ubntu machine





* **Errors while setup and running on local:**
  * SAAS Error -> Run npm rebuild saas
  * Node Fibers Error ->\
    npm uninstall fibers\
    npm install fibers\
    (restart your machine)\
    also please check the terminal for the warning and command suggestions
  * GYP Error -> follow the command suggestion in the terminal
  * Note: please restart system
  *   MAC M1 Error:

      alias python=/usr/bin/python3

      eval "$(pyenv init --path)"

      Mac M1 chip set gives an canvas error which can be solved by following commands

For more details and query please go through the below discussion thread&#x20;

[https://github.com/orgs/Sunbird-coKreat/discussions/65](https://github.com/orgs/Sunbird-coKreat/discussions/65)\
