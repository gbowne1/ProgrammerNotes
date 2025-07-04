# PostgreSQL

This documentation is about using the psql command line.  This is based on some testing I have done.

Check to see if its already installed using `dpkg -l postgresql`

If not installed, use sudo apt update to refresh package lists and then `sudo apt install postgresql postgresql-contrib` to install the server and additional tools.

I strongly advice making a backup of this file just in case.

you can use `ALTER SYSTEM` to make changes.

To reload, `SELECT pg_reload_conf();` will reload the configuration.

Should you want to see any variable, use `SHOW` and the variable name.

## Connecting to a PostgreSQL server and or database

To connect to PostgreSQL, the command in the console/terminal/shell is `psql -U postgres` but this will only connect using the `postgres` user.

Another way you can do it is `psql -h <host> -p <port> -U <username> -d <database_name>`

just replace those placeholders,

    <host>: The server hostname or IP address (usually localhost)
    <port>: The PostgreSQL port (usually 5432)
    <username>: The username you created
    <database_name>: The database name you created

The following command connects to the "gbowne1" database using the "gbowne1" user

`psql -d gbowne1 -U gbowne1`

## Create a database

`createdb <database_name>`(replace <database_name> with your desired database name)

To create a Database with SQL, use `CREATE DATABASE databasename`

`sudo -u postgres createdb` database will create a gbowne1 database.

## Starting PostgreSQL

In Sysvinit, the command to start the PostgreSQL service is: `sudo service postgresql stop` or `sudo service postgresql start`

Normally, PostgreSQL requires systemd to run.  You are better off using sysvinit.

`sudo -u postgres psql -c "COMMAND IN HERE;"`  will issue a SQL syntax.

## using PostgreSQL SQL commands

All `CREATE` SQL commands must end with a semicolon `;`

## PostgreSQL default port

The PostgreSQL default port is 5432, make sure it is enabled in your firewall if you need a remote access.

## Creating or altering a user

To create a new user, `createuser -s <username> (replace <username>` with your desired username)

`psql -c "ALTER USER <username> WITH PASSWORD '<password>';"` (replace <username> and <password> accordingly)

`sudo -u postgres createuser --interactive --pwprompt` will use the interactive prompts to create a user.

In order to change to the postgresql user, `sudo su - postgres`

## Configuration files

The PostgreSQL has several configuration files:

- pg_hba.conf
- postgresql.conf
- pg_ident.conf

The config files live in `/var/lib/postgresql`, but could also be in `/etc/postgresql`

Client configs locally may probably be stored in an rc file at ~/.psqlrc

These configuration files are located in `/etc/postgresql/<version>/main/` each version of postgresql you have installed will have their own
configuration files. (replace or substitute `<version>` with whatever version number you have installed).

There are some parameters that `postgresql.conf` uses:

- listen_addresses 
- port
- shared_buffers
- max-connections
- authentication_methods
- pg_hba_conf
- log_level
- log_line_prefix
- log_filename
- log_destination
- work_mem
- logging_collector
- bgwriter_delay
- maintenance_work_mem
- effective_cache_size
- random_page_cost
- hba_file
- ident_file
- bgwriter_delay
- bgwriter_lru_maxpages


The important ones are listen_addresses, port and max-connection. You could ignore the rest.
effective_cache_size should be 50-75% of total system RAM.

You can use the `ALTER SYSTEM` command with some care taken, to change some behavior.

Make sure you stop and/or restart PostgreSQL after applying changes. It's also wise to make a back up to restore to.


## Exiting psql

Typing `quit` of `\q` in psql will exit. `exit` should work too.

## PostgreSQL flags

Missing flags in this list either did not work, did not return anything when used or simply do not exist, returned as invalid option, etc.
Some flags are the same whether used lower or upper but a few are not.  There are also a few flags that only exist in one case or the other but not both
These flags are only used at the bash or shell prompt, not the repl.

### Lowercase flags

`psql -a` seems to start the repl if used by itself. Cant find any information about this. May not be used at all?

`psql -b` seems to start the repl if used by itself. (possibly no longer used post version 8.0)

`psql -c` requires an argument. This allows you to execute a single SQL statement and then exit the psql client. Must use commands between double quotes

`psql -d` requires an argument. used to specify the  database you want to connect to after launching the psql client. `psql -d <database_name>`

`psql -f` requires an argument. used to execute a sequence of SQL statements from a file. `psql -f <filename>`

`psql -h` this sets the hostname

`psql -l` lists the databases as a table. This does not work in the command line. only in the repl.

`psql -n` seems to start the repl. Deprecated? Possibly a command that got removed/added around version 10.

`psql -o` requires an argument. This is used to redirect the query results to a file.

`psql -p` This sets the port number, usually this follows the `-h` flag.

`psql -q` seems to start the repl but without version or help information. Used to suppress normal output from the psql client, similar to psql -s, but with an  additional twist

`psql -s` seems to start the repl if used by itself.  flag in PostgreSQL is used to suppress normal output from the psql client, including informational messages, headers, and notices.

`psql -t` seems to start the repl if used by itself. used to format your query results in a tabular format.

`psql -v` requires an argument. used to define and set environment variables within your psql session. Different from `-V`

`psql -w` seems to start the repl if used by itself. Used to force write mode when connecting to the server

`psql -x` seems to start the repl if used by itself. Turns on extended mode. Deprecated?

`psql -z` seems to start the repl if used by itself.  Might disable ssl mode? Deprecated?

### Uppercase flags

`psql -A` seems to start the repl.  Might display query results in a single line format.

`psql -E` seems to start the repl if used by itself. Enables echo mode. Useful for debugging or record keeping.

`psql -F` requires an argument. `psql -F <separator> [<query>]` and used to format the output of your query results in a specific way

`psql -H` seems to start the repl if used by itself.  Flag used to set the hostname. `psql -H <hostname>`

`psql -L` requires a argument. Used to list all the available databases on the server you're connected to

`psql -P` requires a argument. This sets the port number, usually this follows the `-H` flag.

`psql -R` requires a argument. Unable to find information about this.

`psql -S` seems to start the repl if used by itself. `psql -S <socket_file_path>` or `psql -S /tmp/postgres.sock -U postgres -d mydb`

`psql -T` requires a argument. used to format your query results in a tabular format

`psql -U` flag for username

`psql -V` reports version information, something like `psql (PostgreSQL) 16.2 (Debian 16.2-1.pgdg100+1)`

`psql -W` prompts for a password `Password:`

`psql -X` seems to start the repl if used by itself. Might turn on extended mode and may be also used in place of `-x`. Deprecated?

## Other commands

\l or \list: List available databases

\du or \list users: List database users

\d              -- List tables, views, and sequences in the current schema

\d+             -- Same as \d, but includes size and extra info

\d tablename    -- Describe a table's columns and types

\d+ tablename   -- Same, with size, storage, and other details

\dt             -- List only tables

\dt+            -- Tables with size info

\dv             -- List only views

\dv+            -- Views with additional info

\di             -- List indexes

\di+            -- Indexes with size and details

\ds             -- List sequences

\ds+            -- Sequences with more info

\df             -- List functions

\df+            -- Functions with details like source and return types

\da             -- List aggregate functions

\dn             -- List schemas

\dT             -- List data types

\dT+            -- Data types with size/storage details

\dc             -- List conversions (used in encoding/locale work)

\dC             -- List casts (type-to-type conversions)

\dd             -- List object descriptions/comments

\ddp            -- Show default privileges

\dL             -- List large objects (LOBs)

\du or \dg      -- List roles and users

\l or \list     -- List databases (not strictly a \d command)

\connect <database_name>

\q or \quit: Exit the psql REPL

\h or \help: Get help on psql commands and syntax (can be followed by a specific command for detailed help)

\set <variable_name> <value>: Set psql variables to control behavior (e.g., \set ECHO all to echo all commands)

\pset format <format>: Set output formatting for query results (e.g., \pset format aligned for aligned output)

## Other stuff

Here are some `\` commands that can be used inside the psql repl, at the `usernamehere=#` prompt.

- \a says Output format is unaligned

- \c reports what user is currently connected to which database(s)

- \d usually reports whether it can find any relations

- \e lets the user change their editor

- \f shows the user their field separator

- \h shows the avaliable SQL commands which have help associated with them

- \i says it needs an argument, unknown right now what that argument is

- \l lists the currentdatabases

- \p usually says the query buffer is empty

- \q exits psql

- \r resets the query buffer

- \s shows command history in the current user(s) database(s)? press q to exit this

- \t says Tuples is on

- \w needs an argument unsure what the argument needed is

- \x says expanded display is on

- \C says Title is unset

- \H says output format is html

- \T is almost the same as \t but it says Table attuributes are unset

Also try out something like:
`psql -H 192.168.1.100 -U postgres -d mydb`

## untested commands and flags

at the `username=#` prompt in the repl;

\o doesn't return invalid option
\z doesn't return invalid option, it seems to print a blank line under it
\g doesn't return invalid option.
