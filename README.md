# dev-env-config

### Install Docker on Debian Jessie  
```apt-get update```  
```apt-get install docker.io```

### Install PostgeSQL on Debian Jessie
```sudo apt-get install postgresql postgresql-client postgresql-contrib libpq-dev```
```sudo apt-get install pgadmin3```
```
sudo -u postgres psql postgres
alter user postgres with password 'postgres';
```

### Install Airflow on Debian Jessie 
```
# default
export AIRFLOW_HOME=~/airflow

# install from pypi using pip
pip install airflow

# initialize the database
airflow initdb

# start the web server, default port is 8080
airflow webserver -p 8080

```
