docker-postgresql-ubuntu
=================

**Note:** You cannot configure its database name, username and password, but it does set up a user called `postgres` (no password) and a database called `postgres` which you can use instead.

PostgreSQL 9.5 for Docker with Ubuntu .

    $ docker run -d -p 5432:5432 -e POSTGRESQL_USER=test -e POSTGRESQL_PASS=PASSWORD -e POSTGRESQL_DB=test kzybala/postgresql
    d123a80cz3469645bnv645234981545f
    
    $ psql -h localhost -U test test
    Password for user test:
    psql (9.5.10)
    SSL connection (protocol: TLSv1.2, cipher: ECDHE-RSA-AES256-GCM-SHA384, bits: 256, compression: off)
    Type "help" for help.    
    
    test=#

## Environment variables

 - `POSTGRESQL_DB`: A database that is automatically created if it doesn't exist. Default: `docker`
 - `POSTGRESQL_USER`: A user to create that has access to the database specified by `POSTGRESQL_DB`. Default: `docker`
 - `POSTGRESQL_PASS`: The password for `POSTGRESQL_USER`. Default: `docker`



