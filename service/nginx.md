# Nginx Commands

## Overview
- [Nginx Commands](#nginx-commands)
  - [Overview](#overview)
  - [Starting Nginx](#starting-nginx)
  - [Stopping Nginx](#stopping-nginx)
  - [Restarting Nginx](#restarting-nginx)
  - [Reloading Nginx](#reloading-nginx)
  - [Checking Nginx Status](#checking-nginx-status)
  - [Testing Nginx Configuration](#testing-nginx-configuration)
  - [Viewing Nginx Version](#viewing-nginx-version)
  - [Displaying Nginx Help](#displaying-nginx-help)
  - [Enabling Nginx on Boot](#enabling-nginx-on-boot)
  - [Disabling Nginx on Boot](#disabling-nginx-on-boot)
  - [Reloading Nginx with Zero Downtime](#reloading-nginx-with-zero-downtime)
  - [502 Bad Gateway Check](#502-bad-gateway-check)
    - [1. Check Nginx Configuration](#1-check-nginx-configuration)
    - [2. Verify Backend Server](#2-verify-backend-server)
    - [3. Check Network Connectivity](#3-check-network-connectivity)
    - [4. Review Logs](#4-review-logs)
    - [5. Configuration Example](#5-configuration-example)
    - [6. Restart Services](#6-restart-services)
    - [7. Additional Troubleshooting](#7-additional-troubleshooting)

## Starting Nginx

To start the Nginx service.

```sh
sudo systemctl start nginx
```

## Stopping Nginx

To stop the Nginx service.

```sh
sudo systemctl stop nginx
```

## Restarting Nginx

To restart the Nginx service, which stops and then starts the service.

```sh
sudo systemctl restart nginx
```

## Reloading Nginx

To reload Nginx configurations without interrupting current connections.

```sh
sudo systemctl reload nginx
```

## Checking Nginx Status

To check the current status of the Nginx service.

```sh
sudo systemctl status nginx
```

## Testing Nginx Configuration

To test the Nginx configuration file for syntax errors.

```sh
sudo nginx -t
```

## Viewing Nginx Version

To check the version of the installed Nginx.

```sh
nginx -v
```

## Displaying Nginx Help

To display the help and available command-line options for Nginx.

```sh
nginx -h
```

## Enabling Nginx on Boot

To enable Nginx to start automatically on system boot.

```sh
sudo systemctl enable nginx
```

## Disabling Nginx on Boot

To disable Nginx from starting automatically on system boot.

```sh
sudo systemctl disable nginx
```

## Reloading Nginx with Zero Downtime

To reload Nginx with zero downtime using the `kill` command.

```sh
sudo kill -HUP $(cat /var/run/nginx.pid)
```

## 502 Bad Gateway Check

A 502 Bad Gateway error indicates that the server, while acting as a gateway or proxy, received an invalid response from an inbound server. Here are several steps to help you diagnose and resolve this issue with your Nginx setup:

### 1. Check Nginx Configuration

Ensure that your Nginx configuration files are correctly set up.

- Test the configuration:

```sh
sudo nginx -t
```

This command will check for any syntax errors in your configuration files. If there are errors, it will provide details to help you locate and fix them.

### 2. Verify Backend Server

Ensure that the backend server (e.g., a Node.js server, PHP-FPM, etc.) that Nginx is proxying to is running and accessible.

- Check the status of the backend server:

```sh
sudo systemctl status <your_backend_service>
```

Replace `<your_backend_service>` with the actual service name.

### 3. Check Network Connectivity

Ensure that Nginx can reach the backend server.

- Use `curl` to check connectivity:

```sh
curl -I http://localhost:<backend_port>
```

Replace `<backend_port>` with the port number your backend server is using.

### 4. Review Logs

Check the Nginx error logs for more detailed information about the error.

- Nginx error log:

```sh
sudo tail -f /var/log/nginx/error.log
```

- Backend server logs (e.g., Node.js, PHP-FPM, etc.):

```sh
sudo tail -f /var/log/<backend_log_file>
```

Replace `<backend_log_file>` with the actual log file name.

### 5. Configuration Example

Ensure your Nginx configuration for the proxy pass is correct. Here is an example configuration for a simple reverse proxy setup:

```sh
server {
    listen 80;
    server_name example.com;

    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

### 6. Restart Services

After making any changes to configuration files, restart Nginx and your backend server.

```sh
sudo systemctl restart nginx
sudo systemctl restart <your_backend_service>
```

### 7. Additional Troubleshooting

If the problem persists, consider these additional steps:

- Ensure that your backend server is not overloaded and has sufficient resources (CPU, memory).
- Check if any firewall rules or security groups are blocking the connection.
- Verify that DNS settings are correctly resolving the backend server's address.

By following these steps, you should be able to identify and resolve the 502 Bad Gateway error in your Nginx setup. If you need further assistance, please provide more details about your specific setup and any relevant configurations or log entries.

This document provides essential commands for managing Nginx, enabling efficient control over your Nginx service.