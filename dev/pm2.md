# PM2 Commands

## Overview
- [PM2 Commands](#pm2-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing PM2](#installing-pm2)
  - [Checking PM2 Version](#checking-pm2-version)
  - [Starting an Application](#starting-an-application)
  - [Stopping an Application](#stopping-an-application)
  - [Restarting an Application](#restarting-an-application)
  - [Listing All Processes](#listing-all-processes)
  - [Monitoring Processes](#monitoring-processes)
  - [Viewing Logs](#viewing-logs)
  - [Setting Up Startup Script](#setting-up-startup-script)
  - [Reloading All Applications](#reloading-all-applications)
  - [Deleting an Application](#deleting-an-application)
  - [Getting Application Info](#getting-application-info)
  - [Generating a Process List](#generating-a-process-list)

## Introduction

PM2 is a production process manager for Node.js applications. It allows you to keep your applications alive forever, reload them without downtime, and facilitate common system admin tasks.

## Installing PM2

To install PM2 globally:

```sh
npm install -g pm2
```

## Checking PM2 Version

To check the version of PM2 installed:

```sh
pm2 --version
```

## Starting an Application

To start a Node.js application with PM2:

```sh
pm2 start app.js
```

Replace `app.js` with the name of your Node.js application file.

## Stopping an Application

To stop a running application:

```sh
pm2 stop app-name-or-id
```

Replace `app-name-or-id` with the name or ID of the application you want to stop.

## Restarting an Application

To restart a running application:

```sh
pm2 restart app-name-or-id
```

Replace `app-name-or-id` with the name or ID of the application you want to restart.

## Listing All Processes

To list all PM2 managed processes:

```sh
pm2 list
```

## Monitoring Processes

To monitor all processes in real-time:

```sh
pm2 monit
```

## Viewing Logs

To view logs for all processes managed by PM2:

```sh
pm2 logs
```

To view logs for a specific application:

```sh
pm2 logs app-name-or-id
```

Replace `app-name-or-id` with the name or ID of the application whose logs you want to view.

## Setting Up Startup Script

To generate and configure a startup script to run PM2 and its managed processes on system startup:

```sh
pm2 startup
```

Follow the instructions provided by the command to set up the startup script.

## Reloading All Applications

To reload all applications managed by PM2 without downtime:

```sh
pm2 reload all
```

## Deleting an Application

To delete an application from PM2's process list:

```sh
pm2 delete app-name-or-id
```

Replace `app-name-or-id` with the name or ID of the application you want to delete.

## Getting Application Info

To get detailed information about a specific application:

```sh
pm2 describe app-name-or-id
```

Replace `app-name-or-id` with the name or ID of the application you want information about.

## Generating a Process List

To generate a process list for use with `pm2 resurrect`:

```sh
pm2 save
```