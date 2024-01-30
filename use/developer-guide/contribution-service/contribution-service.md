# Install Locally

### System Requirements

<table data-header-hidden><thead><tr><th width="323">Softwares / Frameworks</th><th></th></tr></thead><tbody><tr><td>OS</td><td>Ubuntu, linux and Mac</td></tr><tr><td>RAM </td><td>4GB (8GB recommended)</td></tr><tr><td>SSD/HDD</td><td>256 GB</td></tr></tbody></table>

### System Installations

<table><thead><tr><th width="323">Softwares / Frameworks</th><th>Version</th></tr></thead><tbody><tr><td>Node</td><td>10 / 12 / 14</td></tr><tr><td>Postgres</td><td>9.6</td></tr><tr><td>Redis</td><td>4.x or above</td></tr><tr><td>Kafka</td><td>2.4.1</td></tr></tbody></table>

### Installation

The steps to install contribution/program service, are given in here.

### Pre-requisites

1. Make sure you have all the system requirements and system installations to successfully install and run Program Service.
2. Program service uses Postgres database to store and manage data. Refer [programs.sql](https://github.com/Sunbird-Ed/program-service/blob/master/programs.sql) for the database and table structure.

### Project Setup

1. Clone project

```
git clone https://github.com/Sunbird-coKreat/program-service.git
```

> _**Note**_: Stable versions of the sunbird portal are available via tags for each release, and the master branch contains latest stable release.

2. Install Git Submodules to make use of [https://github.com/project-sunbird/sunbird-js-utils.git](https://github.com/project-sunbird/sunbird-js-utils.git)

```
cd {PROJECT-FOLDER}
git submodule init
git submodule update
```

3. Install required dependencies

```
cd {PROJECT-FOLDER}/src
npm install
```

4. Edit the Application Configuration

Open the file `{PROJECT-FOLDER}/src/envVariables.js` in any available text editor and update the contents of the file so that it contains exactly the following values

```
const envVariables = {
baseURL: process.env.dock_base_url || <'https://<host for adopter's coKreat instance'>,
SUNBIRD_URL: process.env.sunbird_base_url || <'https://<host for adopter's sunbird instance'>,
....
config: {
    user: process.env.sunbird_program_db_user || "<postgress user>",
    host: process.env.sunbird_program_db_host || "localhost",
    database: process.env.sunbird_program_db_name || 'sunbird_programs',
    password: process.env.sunbird_program_db_password || '<postgress password>',
   ....
},
}
```

> Once the file is updated with the correct values, you can proceed with running the application

### Running Application

```
cd {PROJECT-FOLDER}/src
node app.js
```

The local HTTP server is launched at `http://localhost:6000`

