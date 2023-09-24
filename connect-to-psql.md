
To connect to PostgreSQL, the command in the console/terminal/shell is `psql -U postgres`

To create a Database, use `CREATE DATABASE databasename`

This command connects to the "gbowne1" database using the "gbowne1" user

`psql -d gbowne1 -U gbowne1`

In Sysvinit, the command to start the PostgreSQL service is: `sudo service postgresql stop` or `sudo service postgresql start`

Normally, PostgreSQL requires systemd to run.

`sudo -u postgres psql -c "COMMAND IN HERE;"`  will issue a SQL syntax.

All CREATE sql commands must end with a ;

The PostgreSQL port is 5432

`sudo -u postgres createdb database will create a gbowne1 database.

`\du` will list the users

`sudo -u postgres createuser --interactive --pwprompt` will use the interative prompts to create a user.

The PostgreSQL has several configuration files:

- pg_hba.conf
- postgresql.conf
-
