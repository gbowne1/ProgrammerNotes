# Configuring MySQL or MariaDB

To configure MySQL or MariaDB in Linux, you can use the option files. The default option
file is called my.cnf (or mariadb.cnf) on Unix-like operating systems and my.ini on Windows

The default location for the option file is /etc/mysql/my.cnf

However, it's important to note that there is also a directory for additional MySQL config files
which is /etc/my.cnf.d

You can use both /etc/my.cnf and files in the /etc/my.cnf.d directory to configure MariaDB.
If settings are set in /etc/my.cnf, they will override other configurations placed inside the /etc/my.cnf.d directory

On Linux systems, the configuration is typically handled via option files, which define various server settings.
📁 Common Configuration File Locations

    Primary configuration file:

        /etc/my.cnf (common on Red Hat/CentOS)

        /etc/mysql/my.cnf (common on Debian/Ubuntu)

    Additional configuration directory:

        /etc/my.cnf.d/ (Red Hat-based systems)

        /etc/mysql/conf.d/ and /etc/mysql/mariadb.conf.d/ (Debian-based systems)

These directories contain additional .cnf files that are loaded in order, allowing modular and organized configuration.
🧠 Precedence Rules

MySQL and MariaDB read configuration files in a specific order. When the same setting appears in multiple places, the last one read wins.

Here's a simplified precedence:

    /etc/my.cnf

    /etc/mysql/my.cnf

    Files in /etc/my.cnf.d/, /etc/mysql/conf.d/, and similar directories

    User-specific files like ~/.my.cnf

⚠️ If the same setting appears in both /etc/my.cnf and a file in /etc/my.cnf.d/, the setting in /etc/my.cnf takes precedence, as it's read later.
