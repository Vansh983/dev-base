# macOS Commands

## Overview
- [macOS Commands](#macos-commands)
  - [Overview](#overview)
  - [Updating and Upgrading Packages with Homebrew](#updating-and-upgrading-packages-with-homebrew)
  - [Installing a Package with Homebrew](#installing-a-package-with-homebrew)
  - [Removing a Package with Homebrew](#removing-a-package-with-homebrew)
  - [Searching for a Package with Homebrew](#searching-for-a-package-with-homebrew)
  - [Viewing Installed Packages with Homebrew](#viewing-installed-packages-with-homebrew)
  - [Checking System Information](#checking-system-information)
  - [Managing Services](#managing-services)
  - [Managing Users](#managing-users)
  - [Checking Disk Usage](#checking-disk-usage)
  - [Viewing System Logs](#viewing-system-logs)
  - [Managing Applications](#managing-applications)

## Updating and Upgrading Packages with Homebrew

To update Homebrew and upgrade all packages to the latest version.

```sh
brew update && brew upgrade
```

## Installing a Package with Homebrew

To install a specific package.

```sh
brew install package-name
```

Replace `package-name` with the name of the package you want to install.

## Removing a Package with Homebrew

To remove a specific package.

```sh
brew uninstall package-name
```

Replace `package-name` with the name of the package you want to remove.

## Searching for a Package with Homebrew

To search for a specific package in the Homebrew repositories.

```sh
brew search package-name
```

Replace `package-name` with the name of the package you are searching for.

## Viewing Installed Packages with Homebrew

To list all installed packages.

```sh
brew list
```

## Checking System Information

To display detailed information about the system.

```sh
system_profiler SPHardwareDataType
```

## Managing Services

To start a service.

```sh
brew services start service-name
```

To stop a service.

```sh
brew services stop service-name
```

To restart a service.

```sh
brew services restart service-name
```

To check the status of a service.

```sh
brew services list
```

Replace `service-name` with the name of the service you want to manage.

## Managing Users

To add a new user.

```sh
sudo dscl . -create /Users/username
sudo dscl . -create /Users/username UserShell /bin/bash
sudo dscl . -create /Users/username RealName "User Name"
sudo dscl . -create /Users/username UniqueID 1001
sudo dscl . -create /Users/username PrimaryGroupID 80
sudo dscl . -create /Users/username NFSHomeDirectory /Users/username
sudo dscl . -passwd /Users/username password
sudo createhomedir -c -u username
```

To delete a user.

```sh
sudo dscl . -delete /Users/username
```

Replace `username` with the name of the user you want to add or delete, and replace `password` with the user's password.

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
log show
```

To view the most recent logs.

```sh
log show --predicate 'eventMessage contains "error"' --info --last 24h
```

## Managing Applications

To list all installed applications.

```sh
ls /Applications
```

To open a specific application.

```sh
open -a "Application Name"
```

Replace `Application Name` with the name of the application you want to open.