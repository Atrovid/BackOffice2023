Welcome to your new dbt project!

## Prerequesites

### Prerequesites software

Install :
- Docker software

### Prerequesites files

In the database_bo folder (~/backoffice2023/Back-End/database_bo):
- add a new file called docker-compose.yml and file up this file with relevant informations (such as username and passwaord) given by the database manager
- add a new file called Dockerfile, used for creating a virtual docker image, ask for database manager for more informations.

In the profiles folder (~/backoffice2023/Back-End/database_bo/profiles), add a new file called profiles.yml and file up this file with relevant informations (such as username and passwaord) given by the database manager

### Running the virtual image with docker 

In the database_bo folder (~/backoffice2023/Back-End/database_bo), open a terminal and write the following commands in the terminal:

``bash
docker-compose build``

``bash
docker-compose up``

The commands above will run a Postgres instance and then build the dbt ressources of Back-office.
These containers will remain up and running so that you can:

- Query the Postgres database and the tables created out of dbt models
- Run further dbt commands via dbt CLI

### Querying on Postgres

In the database_bo folder (~/backoffice2023/Back-End/database_bo) :

Find the container id of the postgres service :

``bash
docker ps``

Then run

``bash
docker exec -it <container-id> /bin/bash``

We will then use psql, a terminal-based interface for PostgreSQL that allows us to query the database:

``bash
psql -U <username>``

### Using the starter project

Try running the following commands:
- dbt run
- dbt test


### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [chat](https://community.getdbt.com/) on Slack for live discussions and support
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices
