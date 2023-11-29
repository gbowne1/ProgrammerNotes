# Configuring MySQL or MariaDB

To configure MySQL or MariaDB in Linux, you can use the option files. The default option
file is called my.cnf (or mariadb.cnf) on Unix-like operating systems and my.ini on Windows

The default location for the option file is /etc/mysql/my.cnf

However, it's important to note that there is also a directory for additional MySQL config files
which is /etc/my.cnf.d

You can use both /etc/my.cnf and files in the /etc/my.cnf.d directory to configure MariaDB.
If settings are set in /etc/my.cnf, they will override other configurations placed inside the /etc/my.cnf.d directory
