# Apache Commands for Linux

## Overview
- [Apache Commands for Linux](#apache-commands-for-linux)
  - [Overview](#overview)
  - [Installing Apache](#installing-apache)
  - [Starting Apache](#starting-apache)
  - [Stopping Apache](#stopping-apache)
  - [Restarting Apache](#restarting-apache)
  - [Reloading Apache](#reloading-apache)
  - [Checking Apache Status](#checking-apache-status)
  - [Testing Apache Configuration](#testing-apache-configuration)
  - [Enabling a Site](#enabling-a-site)
  - [Disabling a Site](#disabling-a-site)
  - [Enabling a Module](#enabling-a-module)
  - [Disabling a Module](#disabling-a-module)
  - [Viewing Apache Logs](#viewing-apache-logs)
  - [Configuring Virtual Hosts](#configuring-virtual-hosts)
  
## Installing Apache

To install Apache on a Debian-based Linux system (e.g., Ubuntu):

```sh
sudo apt update
sudo apt install apache2
```

To install Apache on a Red Hat-based Linux system (e.g., CentOS):

```sh
sudo yum install httpd
```

## Starting Apache

To start the Apache server on Debian-based systems:

```sh
sudo systemctl start apache2
```

To start the Apache server on Red Hat-based systems:

```sh
sudo systemctl start httpd
```

## Stopping Apache

To stop the Apache server on Debian-based systems:

```sh
sudo systemctl stop apache2
```

To stop the Apache server on Red Hat-based systems:

```sh
sudo systemctl stop httpd
```

## Restarting Apache

To restart the Apache server on Debian-based systems:

```sh
sudo systemctl restart apache2
```

To restart the Apache server on Red Hat-based systems:

```sh
sudo systemctl restart httpd
```

## Reloading Apache

To reload the Apache server configuration without restarting on Debian-based systems:

```sh
sudo systemctl reload apache2
```

To reload the Apache server configuration without restarting on Red Hat-based systems:

```sh
sudo systemctl reload httpd
```

## Checking Apache Status

To check the status of the Apache server on Debian-based systems:

```sh
sudo systemctl status apache2
```

To check the status of the Apache server on Red Hat-based systems:

```sh
sudo systemctl status httpd
```

## Testing Apache Configuration

To test the Apache configuration for syntax errors on Debian-based systems:

```sh
sudo apache2ctl configtest
```

To test the Apache configuration for syntax errors on Red Hat-based systems:

```sh
sudo httpd -t
```

## Enabling a Site

To enable a site on Debian-based systems (using a2ensite):

```sh
sudo a2ensite site-name.conf
```

Replace `site-name.conf` with the name of your site's configuration file.

## Disabling a Site

To disable a site on Debian-based systems (using a2dissite):

```sh
sudo a2dissite site-name.conf
```

Replace `site-name.conf` with the name of your site's configuration file.

## Enabling a Module

To enable a module on Debian-based systems (using a2enmod):

```sh
sudo a2enmod module-name
```

Replace `module-name` with the name of the module you want to enable.

## Disabling a Module

To disable a module on Debian-based systems (using a2dismod):

```sh
sudo a2dismod module-name
```

Replace `module-name` with the name of the module you want to disable.

## Viewing Apache Logs

To view the Apache access log on Debian-based systems:

```sh
sudo tail -f /var/log/apache2/access.log
```

To view the Apache error log on Debian-based systems:

```sh
sudo tail -f /var/log/apache2/error.log
```

To view the Apache access log on Red Hat-based systems:

```sh
sudo tail -f /var/log/httpd/access_log
```

To view the Apache error log on Red Hat-based systems:

```sh
sudo tail -f /var/log/httpd/error_log
```

## Configuring Virtual Hosts

To configure virtual hosts, create a new configuration file in the Apache configuration directory (e.g., `/etc/apache2/sites-available/` on Debian-based systems or `/etc/httpd/conf.d/` on Red Hat-based systems):

For Debian-based systems:

```sh
sudo nano /etc/apache2/sites-available/site-name.conf
```

For Red Hat-based systems:

```sh
sudo nano /etc/httpd/conf.d/site-name.conf
```

Add the following configuration to the file:

```apache
<VirtualHost *:80>
    ServerAdmin webmaster@site-name.com
    ServerName site-name.com
    ServerAlias www.site-name.com
    DocumentRoot /var/www/site-name
    ErrorLog ${APACHE_LOG_DIR}/site-name_error.log
    CustomLog ${APACHE_LOG_DIR}/site-name_access.log combined
</VirtualHost>
```

Replace `site-name` with your site's name and adjust paths and settings as necessary.

Enable the site and reload Apache:

For Debian-based systems:

```sh
sudo a2ensite site-name.conf
sudo systemctl reload apache2
```

For Red Hat-based systems:

```sh
sudo systemctl reload httpd
```