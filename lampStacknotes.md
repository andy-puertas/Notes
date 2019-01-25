### Lamp Stack


### Setting up a LAMP Stack
***
##### lamp stack

The LAMP stack consits of:
* Linux
* Apache
* mySQL database
* php
***
On top of the lamp stack, we will install **WordPress**
***

First, let's get the stack up and running

***
1. Install Ubuntu 16 or 18 (mysql root user issue)
2. update Ubuntu `sudo apt-get update`
3. Install the Apache2 Webserver `sudo apt install apache2`
4. install Mysql server `sudo apt install mysql-server`
5. Set up the password for the root user inside mysql
6. Install the necessary php add-ons `sudo apt install php-pear php-fpm php-dev php-zip php-curl php-xmlrpc php-gd php-mysql php-mbstring php-xml libapache2-mod-php`
7. restart Apache with `sudo service apache2 restart`
8. Check to see if things are working by navigating to http://127.0.0.1 or http://localhost. You should see the default Apache index.html file



Now we are going to set up our own php page and configure Apache to point to it.  Apache stores web pages in `/var/www/html`.  We need to change the ownership and permissions of that directory.

1. `cd /var` will put us into the `var` directory.  `sudo chown -R jakeryan www` will change the owner to jakeryan for `www` and all the files inside.  The -R stands for *`R`ecursive*
1. we also need to change the group to your username.  `sudo chgrp -R jakeryan www`
1. `cd /etc/apache2/conf-enabled` so we can make a *symbolic link*
1. `sudo ln -s ../conf-availabe/php7.0-fpm.conf` the benefit of linking these conf files over copying them, is that you don't have to store multiple copies of the exact same thing.
1. edit the apache config file document root `cd /etc/apache2/sites-enabled` `sudo nano 000-default.conf`
1. change the line `DocumentRoot var/www/html` to `DocumentRoot var/www`
1. `sudo service apache2 restart`

##### Word Press Installation

1. `cd` to get into home directory
1. install **curl** with `sudo apt install curl`
1. install WP `curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar`
1. `chmod +x wp-cli.phar`
1. `sudo mv wp-cli.phar /usr/local/bin/wp`
1. `cd /var/www` `mkdir mysite`
1. `cd mysite`
1. `wp core download`

***

##### Setting up mySQL for WP

log into mySQL as root user using the password from earlier, then create a new database.

1. `mysql -u root -p`
1. You should be inside mysql.  it should say mysql in the terminal.
1. `CREATE DATABASE WP_mysite;`
1. go to localhost/mysite in your browser.  It will run you through the wp setup.  If it doesn't create conf file, copy all the text and ` cd /var/www/mysite`
1. `sudo nano wp-config.php`
1. paste in the text and save.  localhost/mysite should now be your website.
