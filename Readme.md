# Simple Docker Webserver (Nginx, PHP, MariaDB, Xdebug)

This webserver contains a basic configuration with

* nginx (latest)
* php (7-fpm) - configured with xdebug
* mariadb (latest)

## Configurate your environment

### PHP Settings

The default xdebug port is set to 9001. Make sure that you change the IP address to your local IP address you will get 
with the `ifconfig` command on your console. You have to change it in the file  `conf / php / php.ini`.

`xdebug.remote_host={YOUR-IP-ADDRESS}`

Also you can setup further xdebug or php settings in the php.ini file.

### PhpStorm Settings

Enter the remote host port in `PhpStorm > Preferences` under the nodes Languages and `Frameworks > PHP > Debug` in 
the field `XDebug > Debug Port` to the port you have entered at your php.ini.

### Webserver settings

The nginx host by default is `localhost`. You can change the host it in the  `conf / nginx / nginx.conf`. But please 
keep in mind to add the host entry to your local `/etc/hosts` file.

## Launching Webserver

Start the webserver with the command `docker-compose up` and stop it with `docker-compose down`.

