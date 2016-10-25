# dev-env-config

#Docker
## Install Docker on Debian Jessie  
```
apt-get update  
apt-get install docker.io
```
#PostgeSQL
## Install PostgeSQL on Debian Jessie
```
sudo apt-get install postgresql postgresql-client postgresql-contrib libpq-dev```
sudo apt-get install pgadmin3
sudo -u postgres psql postgres
alter user postgres with password 'postgres';
```

#Airflow
```
                            ____________       _____________
                           ____    |__( )_________  __/__  /________      __
                          ____  /| |_  /__  ___/_  /_ __  /_  __ \_ | /| / /
                          ___  ___ |  / _  /   _  __/ _  / / /_/ /_ |/ |/ /
                           _/_/  |_/_/  /_/    /_/    /_/  \____/____/|__/

```
## Install Airflow on Debian Jessie 
```
# default
export AIRFLOW_HOME=~/airflow

# install from pypi using pip
pip install airflow

# initialize the database
airflow initdb

# postgres and vertica operators and hook, support as an Airflow backend
pip install airflow[postgres]
pip install airflow[vertica]

airflow version
```

## Airflow Comand Line Interface 
```
# start the web server, default port is 8080
airflow webserver -p 8080

# run a single task instance
airflow run dag_id task_id execution_date

# list the tasks within a DAG
airflow list_tasks dag_id

# list all the DAGs
airflow list_dags
```
