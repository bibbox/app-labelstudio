# labelstudio BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX App Store") or standalone. 

After the docker installation follow these [instructions](INSTALL-APP.md).

## Standalone Installation 

Clone the github repository. If necessary change the ports in the environment file `.env` and the volume mounts in `docker-compose.yml`.

```
git clone https://github.com/bibbox/app-labelstudio
cd app-labelstudio
docker network create bibbox-default-network
docker-compose up -d
```

The main App can be opened and set up at:
```
http://localhost:8080
```

## Install within BIBBOX

Visit the BIBBOX page and find the App by its name in the store. Click on the symbol and select install. Then fill the parameters below and name your App, click install again.

## Docker Images used
  - [heartexlabs/label-studio](https://hub.docker.com/r/heartexlabs/label-studio) 
  - [heartexlabs/label-studio](https://hub.docker.com/r/heartexlabs/label-studio) 
  - [postgres](https://hub.docker.com/r/postgres) 


 
## Install Environment Variables
  - POSTGRE_PASSWORD = User's password

  
The default values for the standalone installation are:
  - POSTGRE_PASSWORD = changethispasswordinproductionenvironments

  
## Mounted Volumes
### heartexlabs/label-studio Container
  - *./data/mydata:/label-studio/data:rw*
  - *./data/deploy/nginx/certs:/certs:ro*
### heartexlabs/label-studio Container
  - *./data/data/container/app-data:/app-data*
### postgres Container
  - *./data/postgres-data:/var/lib/postgresql/mydata:z*
  - *./data/deploy/pgsql/certs:/var/lib/postgresql/certs:ro*

