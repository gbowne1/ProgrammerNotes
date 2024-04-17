# Connecting to PostgreSQL.

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

The PostgreSQL has a couple configuration files:

- pg_hba.conf
- postgresql.conf

The config files live in /var/lib/postgresql

This path is usually followed by the version number.  Look in the following /data directory for the *two .conf files.

Client configs locally may probably be stored in ~/.psqlrc

## configuration files

- postgresql.conf

There are some parameters that this file uses:

  - listen_addresses:
  - port:
  - shared_buffers:
  - max-connections:
  - authentication_methods:
  - pg_hba_conf
  - log_level
  - log_line_prefix
  - log_destination

There are others.  Refer to the official configuration documents.

- pg_hba.conf

This file is mainly used for securing PostgreSQL. It's essentially a list who & what can access the database
