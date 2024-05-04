# Configuring Apache2


## Virtual Hosts

An Apache2 virtual host is a powerful feature that allows you to host multiple websites (or applications) on a single server using a single Apache2 instance. It essentially tricks your server into thinking it's serving content from multiple machines, even though it's all on the same physical hardware.

When a user accesses a website, their browser sends a request specifying the domain name (e.g., `www.example.com`). Apache2 uses virtual hosts to determine which website's content to serve based on the requested domain name.

- /etc/apache2/sites-available/*.conf: These files define configurations for individual websites or applications hosted on your server. The naming convention is typically `*.conf`, and they reside in the sites-available directory. There can be multiple virtual host files depending on how many websites you plan to host.
- /etc/apache2/sites-enabled/*.conf: This directory contains symlinks to the virtual host configuration files from sites-available that are currently active.

There are some module configuration files.

- /etc/apache2/mods-available/*.load: These files with the .load extension enable specific Apache2 modules. Debian manages Apache2 modules by keeping track of enabled and available modules in separate directories.

- /etc/apache2/mods-enabled/*.conf: These files contain configurations for the enabled modules and reside in the mods-enabled directory.

Additional configuration files may be located in the /etc/apache2/conf-available/ directory. These files can contain snippets for various functionalities and are enabled by creating symlinks in the conf-enabled directory.

You really shouldn't directly modify the files in the sites-available and mods-available directories unless you know your way around Apache2.

Instead, use the a2ensite and a2enmod commands to enable them by creating symlinks in the corresponding enabled directories.

The Apache2 package provides utilities like a2ensite and a2enmod to manage these configuration files easily.

For further details on configuring Apache2 virtual hosts and modules, refer to the Apache documentation or search online resources specific to Debian 10 Buster.

In Apache2, you need to have an apache2.conf in /etc/apache2, This is the core configuration file that holds the overall settings for Apache2. It includes other configuration files and defines the global behavior of the web server.

Apache2 generally requires the use of systemd, which is quite sad.

If you use SysVinit, in order to check status, restart, etc. you need to issue

`sudo /etc/init.d/apache2 restart`

`sudo /etc/init.d/apache2 status`

## Logging in Apache2

Apache2 logs go into /var/log/apache2

The /var/log/apache2 needs to have the right owner and permissions.

check to see if it is

`ls -ld /var/log/apache2/`

drwxrwxr-x 2 www-data www-data 4096 Apr 16 14:27 /var/log/apache2/

if it is not, just issue this command

`sudo chown www-data:www-data /var/log/apache2/`

also change the perms using

`sudo chmod g+rw /var/log/apache2/`

Logs may not work if you tail them with

`sudo tail /var/log/apache2/error_log`

if that  does not work you can

`sudo cat /var/log/apache2/error.log`

The logs it should  create are:

access.log
error.log
other_vhosts_access.log

## Specifying Log files

Specifying Log Files:

The CustomLog and ErrorLog directives specify the location and format for access and error logs, respectively. You can use them in apache2.conf for global settings or within virtual host configuration files.

Here's an example of configuring a custom access log for a virtual host:

<VirtualHost *:80>
  ServerName yourdomain.com
  DocumentRoot /var/www/html/yourdomain.com
  CustomLog /var/log/apache2/yourdomain_access.log custom_format
  ErrorLog /var/log/apache2/yourdomain_error.log
</VirtualHost>

## Customizing the log format

The LogFormat directive in apache2.conf defines the format for log entries. By default, Apache2 uses the "Common Log Format" (CLF), but you can create custom formats to capture specific data points.

Here's an example of modifying the LogFormat directive

LogFormat "%h %l %u %t \"%r\" %>s %O \"%{Referer}i\" \"%{User-Agent}i\"" custom_format

This format captures additional information like referrer URL and user agent compared to the default CLF.

## Where the code for your site goes

Your website or webapp code goes in:

/var/www/html
/var/www
/public_html
/usr/share (for WebApps)

navigate your favorite browser to localhost: and you should see the Apache2 template page
