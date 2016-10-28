# dev-env-config

#Docker
```
                                                    ##        .            
                                              ## ## ##       ==            
                                           ## ## ## ##      ===            
                                       /""""""""""""""""\___/ ===        
                                  ~~~ {~~ ~~~~ ~~~ ~~~~ ~~ ~ /  ===- ~~~   
                                       \______ o          __/            
                                         \    \        __/             
                                          \____\______/                

                                          |          |
                                       __ |  __   __ | _  __   _
                                      /  \| /  \ /   |/  / _\ | 
                                      \__/| \__/ \__ |\_ \__  |
```
## Install Docker on Debian Jessie  
```
apt-get update  
apt-get install docker.io
```
#PostgeSQL
```
                                      +------------------------+
                                      |   ____  ______  ___    |
                                      |  /    )/      \/   \   |
                                      | (     / __    _\    )  |
                                      |  \    (/ o)  ( o)   )  |
                                      |   \_  (_  )   \ ) _/   |
                                      |     \  /\_/    \)/     |
                                      |      \/ <//|  |\\>     |
                                      |           _|  |        |
                                      |           \|_/         |
                                      |                        |
                                      |  PostgreSQL 1996-2016  |
                                      |  20 years of success   |
                                      +------------------------+
```
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

# run subsections of a DAG for a specified date rang
airflow backfill dag_id -s 28.10.2016 -e 28.10.2016

# individual tasks can be tested also
airflow test HelloWorld task_1 2016-04-15
```
