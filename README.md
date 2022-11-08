# Label Studio BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX") or standalone.
 
After the installation follow these [instructions](INSTALL-APP.md)

## Hints

* approx. time with medium fast internet connection: **5 minutes**

## Install within BIBBOX

Within BIBBOX you can use the [BIBBOX](https://bibbox.readthedocs.io/en/latest/ "BIBBOX") to install a lot of software tools. After the installation is finished you can start your application in the dashboard.

### Install Environment Variables

 * POSTGRE_PASSWORD: POSTGRES database password
 



## Docker Images Used

 * [postgres](https://hub.docker.com/_/postgres, offical postgres container
 * [labelstudio] https://hub.docker.com/r/heartexlabs/label-studio, oficial labelstudio docker image
 
## Standalone Installation

To install the app locally execute the commands:

* Clone the git repository: 
  * `git clone https://github.com/bibbox/app-labelstudio.git`
* Change the current directory to app-labelstudio: 
  * `cd app-labelstudio/` 
* Create the directories `PATH1`, `PATH2` and `PATH3`: 
  * `mkdir -p data` 
  

* Create the docker network `bibbox-default-network`: 
  * `docker network create bibbox-default-network`
* Run **docker-compose up** in the root folder of the project: 
  * `docker-compose up -d`

## Mounted Volumes

* /data/data/container/app-data
* /data/deploy/nginx
* /data/deploy/pgsql
* /data/mydata
* /data/postgres-data
