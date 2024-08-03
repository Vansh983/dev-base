# ngrok Commands

## Overview
- [ngrok Commands](#ngrok-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing ngrok](#installing-ngrok)
  - [Connecting ngrok to Your Account](#connecting-ngrok-to-your-account)
  - [Starting an HTTP Tunnel](#starting-an-http-tunnel)
  - [Starting a TCP Tunnel](#starting-a-tcp-tunnel)
  - [Starting an HTTPS Tunnel](#starting-an-https-tunnel)
  - [Viewing Tunnel Status](#viewing-tunnel-status)
  - [Inspecting Traffic](#inspecting-traffic)
  - [Configuring ngrok with a YAML File](#configuring-ngrok-with-a-yaml-file)
  - [Stopping ngrok](#stopping-ngrok)

## Introduction

ngrok is a reverse proxy that creates a secure tunnel from a public endpoint to a locally running web service. It captures and analyzes all traffic over the tunnel for later inspection and replay.

## Installing ngrok

To install ngrok, download the binary for your operating system from the [official ngrok website](https://ngrok.com/download) and follow the installation instructions.

For example, on macOS:

```sh
brew install --cask ngrok
```

## Connecting ngrok to Your Account

To connect ngrok to your account, use the authtoken provided on your ngrok dashboard:

```sh
ngrok config add-authtoken YOUR_AUTHTOKEN
```

Replace `YOUR_AUTHTOKEN` with the authtoken from your ngrok dashboard.

## Starting an HTTP Tunnel

To start an HTTP tunnel:

```sh
ngrok http 80
```

Replace `80` with the port number your web service is running on.

## Starting a TCP Tunnel

To start a TCP tunnel:

```sh
ngrok tcp 22
```

Replace `22` with the port number your service is running on.

## Starting an HTTPS Tunnel

To start an HTTPS tunnel, you can specify the `https` parameter:

```sh
ngrok http https://localhost:443
```

Replace `443` with the port number your HTTPS service is running on.

## Viewing Tunnel Status

To view the status of your ngrok tunnels:

```sh
ngrok status
```

## Inspecting Traffic

ngrok provides a web interface to inspect traffic. By default, this is available at:

```sh
http://localhost:4040
```

You can open this URL in your web browser to inspect requests and responses.

## Configuring ngrok with a YAML File

You can configure ngrok using a `ngrok.yml` configuration file. Create the file and add your desired configuration. For example:

```yaml
authtoken: YOUR_AUTHTOKEN
tunnels:
  http-tunnel:
    proto: http
    addr: 80
  tcp-tunnel:
    proto: tcp
    addr: 22
```

To start ngrok with the configuration file:

```sh
ngrok start --all
```

## Stopping ngrok

To stop ngrok, simply terminate the process by pressing `Ctrl+C` in the terminal where ngrok is running.