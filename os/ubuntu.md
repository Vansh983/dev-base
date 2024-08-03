# Ubuntu Commands

## Overview
- [Ubuntu Commands](#ubuntu-commands)
  - [Overview](#overview)
  - [Updating and Upgrading Packages](#updating-and-upgrading-packages)
  - [Installing a Package](#installing-a-package)
  - [Removing a Package](#removing-a-package)
  - [Searching for a Package](#searching-for-a-package)
  - [Viewing Installed Packages](#viewing-installed-packages)
  - [Checking System Information](#checking-system-information)
  - [Managing Services](#managing-services)
  - [Managing Users](#managing-users)
  - [Checking Disk Usage](#checking-disk-usage)
  - [Viewing System Logs](#viewing-system-logs)

## Updating and Upgrading Packages

To update the package lists and upgrade all packages to the latest version.

```sh
sudo apt update && sudo apt upgrade
```

## Installing a Package

To install a specific package.

```sh
sudo apt install package-name
```

Replace `package-name` with the name of the package you want to install.

## Removing a Package

To remove a specific package.

```sh
sudo apt remove package-name
```

Replace `package-name` with the name of the package you want to remove.

## Searching for a Package

To search for a specific package in the repositories.

```sh
apt search package-name
```

Replace `package-name` with the name of the package you are searching for.

## Viewing Installed Packages

To list all installed packages.

```sh
dpkg --list
```

## Checking System Information

To display detailed information about the system.

```sh
uname -a
```

## Managing Services

To start a service.

```sh
sudo systemctl start service-name
```

To stop a service.

```sh
sudo systemctl stop service-name
```

To restart a service.

```sh
sudo systemctl restart service-name
```

To check the status of a service.

```sh
sudo systemctl status service-name
```

Replace `service-name` with the name of the service you want to manage.

## Managing Users

To add a new user.

```sh
sudo adduser username
```

To delete a user.

```sh
sudo deluser username
```

Replace `username` with the name of the user you want to add or delete.

## Checking Disk Usage

To check disk usage of the file system.

```sh
df -h
```

To check disk usage of a specific directory.

```sh
du -sh directory-name
```

Replace `directory-name` with the path to the directory you want to check.

## Viewing System Logs

To view system logs.

```sh
sudo journalctl
```

To view the most recent logs.

```sh
sudo journalctl -r
```