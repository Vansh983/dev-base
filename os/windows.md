# Windows Commands

## Overview
- [Windows Commands](#windows-commands)
  - [Overview](#overview)
  - [Checking System Information](#checking-system-information)
  - [Managing Services](#managing-services)
  - [Managing Users](#managing-users)
  - [Checking Disk Usage](#checking-disk-usage)
  - [Viewing System Logs](#viewing-system-logs)
  - [Installing Software](#installing-software)
  - [Uninstalling Software](#uninstalling-software)
  - [Managing Network Settings](#managing-network-settings)
  - [Managing Processes](#managing-processes)
  - [Managing Files and Directories](#managing-files-and-directories)

## Checking System Information

To display detailed information about the system.

```sh
systeminfo
```

## Managing Services

To start a service.

```sh
net start "service-name"
```

To stop a service.

```sh
net stop "service-name"
```

To check the status of a service.

```sh
sc query "service-name"
```

Replace `service-name` with the name of the service you want to manage.

## Managing Users

To add a new user.

```sh
net user username password /add
```

To delete a user.

```sh
net user username /delete
```

Replace `username` with the name of the user you want to add or delete, and replace `password` with the user's password.

## Checking Disk Usage

To check disk usage of all drives.

```sh
wmic logicaldisk get size,freespace,caption
```

## Viewing System Logs

To view system logs.

```sh
eventvwr
```

This command opens the Event Viewer, where you can browse various system logs.

## Installing Software

To install software using PowerShell.

```sh
Start-Process "msiexec.exe" -ArgumentList "/i path-to-msi-file /quiet /norestart" -NoNewWindow -Wait
```

Replace `path-to-msi-file` with the path to the MSI file you want to install.

## Uninstalling Software

To uninstall software using PowerShell.

```sh
Get-WmiObject -Query "SELECT * FROM Win32_Product WHERE Name = 'software-name'" | ForEach-Object { $_.Uninstall() }
```

Replace `software-name` with the name of the software you want to uninstall.

## Managing Network Settings

To display IP configuration.

```sh
ipconfig /all
```

To release the current IP address.

```sh
ipconfig /release
```

To renew the IP address.

```sh
ipconfig /renew
```

## Managing Processes

To list all running processes.

```sh
tasklist
```

To kill a specific process.

```sh
taskkill /F /PID process-id
```

Replace `process-id` with the ID of the process you want to kill.

## Managing Files and Directories

To list files in a directory.

```sh
dir
```

To create a new directory.

```sh
mkdir directory-name
```

To delete a directory.

```sh
rmdir /S /Q directory-name
```

Replace `directory-name` with the name of the directory you want to create or delete.

To copy a file.

```sh
copy source-file destination-directory
```

Replace `source-file` with the path to the file you want to copy, and replace `destination-directory` with the path to the destination directory.

To move a file.

```sh
move source-file destination-directory
```

Replace `source-file` with the path to the file you want to move, and replace `destination-directory` with the path to the destination directory.