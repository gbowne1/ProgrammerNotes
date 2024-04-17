In Apache2, you need to have an apache2.conf in /etc/apache2 

Apache2 generally requires the use of systemd, which is quite sad.

If you use SysVinit, in order to check status, restart, etc. you need to issue

sudo /etc/init.d/apache2 restart
sudo /etc/init.d/apache2 status

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

site code goes in:

/var/www/html
/var/www
/public_html
/usr/share (for WebApps)

navigate your favorite browser to localhost: and you should see the Apache2 template page

