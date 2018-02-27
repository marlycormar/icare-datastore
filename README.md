# Getting started #

Make sure you have docker, docker-compose and an internet connection.

Copy the `fake.env` file and rename it to `.env`.

Fill in the correct info. If you decide to change the password for redash in the connection string
make sure to change in in `/initsql/redash.sql`.

Run `docker-compose up --build`

Go to `localhost:8080` and log into redash!

# Adding a datasource #

When using redash and adding a datasource you have two options. One is to use the postgres instance and
information, the other is to add the sqlite databases that are made by quail itself.

## Postgres databases ##

The only thing to note here is that the hostname of the postgres instance is the same as the key of the
service in the `docker-compose.yaml` file.

## Sqlite database ##

You can add the sqlite databases themselves as a redash datasource because they are mounted in the redash
container at `/quail_data`