# Simple Docker Webserver (Nginx, PHP, MariaDB, Xdebug)

This webserver contains a basic configuration with

* nginx (latest)
* php (7-fpm) - configured with xdebug
* mariadb (latest)

The xdebug is configured with the remote port 9000. To configure for your environment, you have to **change the IP address** 
in the docker-compose.yml to your local IP address in the following line:

`XDEBUG_CONFIG: remote_host={YOUR-IP-ADDRESS}`

You will get your local IP address with *ifconfig* on your console.

Start the webserver with the command `docker-compose up` and stop it with `docker-compose down`.