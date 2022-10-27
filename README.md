# Template BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX") or standalone.
 
After the installation follow these [instructions](INSTALL-APP.md)

## Hints

* approx. time with medium fast internet connection: **5 minutes**
* initial user/password: e.g. **admin / admin**

## Install within BIBBOX

Within BIBBOX you can use the [BIBBOX](https://bibbox.readthedocs.io/en/latest/ "BIBBOX") to install a lot of software tools. After the installation is finished you can start your application in the dashboard.

### Install Environment Variables

List of environment parameters set during installation

 * NAME_AS_IN_DOCKER_TEMPLATE_1: ...
 * MYSQL_DATABASE_NAME: ...
 * MYSQL_DATABASE_USER: ...
 * MYSQL_DATABASE_PASSWORD: ...

The default values for the standalone installation are:

 * NAME_AS_IN_DOCKER_TEMPLATE_1: Default Value
 * MYSQL_DATABASE_NAME: Default Value
 * MYSQL_DATABASE_USER: Default Value
 * MYSQL_DATABASE_PASSWORD: Default Value


## Docker Images Used

 * [BIBBOX/imagename](https://hub.docker.com/r/bibbox/imagename) 
 * [mySQL](https://hub.docker.com/_/mysql/), offical mySQL container
 
## Standalone Installation

To install the app locally execute the commands:

* Clone the git repository: 
  * `git clone https://github.com/bibbox/app-template.git`
* Change the current directory to app-template: 
  * `cd app-molgenis/` 
* Create the directories `PATH1`, `PATH2` and `PATH3`:
  * `mkdir -p PATH1` 
  * `mkdir -p PATH2`
  * `mkdir -p PATH3`
* Change the permission of the directories `PATH1`, `PATH2` and `PATH3`: 
  * `chmod -R NUMERIC_VALUE_OF_PERMISSION1 PATH1`
  * `chmod -R NUMERIC_VALUE_OF_PERMISSION2 PATH2`
  * `chmod -R NUMERIC_VALUE_OF_PERMISSION3 PATH3`
* Create the docker network `bibbox-default-network`: 
  * `docker network create bibbox-default-network`
* Run **docker-compose up** in the root folder of the project: 
  * `docker-compose up -d`
* **Alternatively** on a *Linux* system run the bash script `intsall.sh` after cloning and change the working directory to the git repository directory.

## Mounted Volumes

* `PATH1`
* `PATH2`
* `PATH3`
