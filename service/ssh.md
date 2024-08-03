# SSH Commands

## Overview
- [SSH Commands](#ssh-commands)
  - [Overview](#overview)
  - [Installing SSH](#installing-ssh)
  - [Generating SSH Keys](#generating-ssh-keys)
  - [Copying SSH Key to Remote Server](#copying-ssh-key-to-remote-server)
  - [Connecting to a Remote Server](#connecting-to-a-remote-server)
  - [SSH Configuration File](#ssh-configuration-file)
  - [Transferring Files with SCP](#transferring-files-with-scp)
  - [Transferring Files with SFTP](#transferring-files-with-sftp)
  - [Tunneling with SSH](#tunneling-with-ssh)
  - [Forwarding SSH Agent](#forwarding-ssh-agent)
  - [Managing Known Hosts](#managing-known-hosts)
  - [Disabling SSH Root Login](#disabling-ssh-root-login)
  - [Restarting SSH Service](#restarting-ssh-service)

## Installing SSH

SSH is usually pre-installed on most Unix-based systems. To install SSH on a Debian-based system:

```sh
sudo apt update
sudo apt install openssh-server
```

To install SSH on a Red Hat-based system:

```sh
sudo yum install openssh-server
```

## Generating SSH Keys

To generate a new SSH key pair:

```sh
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Follow the prompts to save the key in the default location (`~/.ssh/id_rsa`) and set a passphrase.

## Copying SSH Key to Remote Server

To copy your SSH public key to a remote server:

```sh
ssh-copy-id user@remote_host
```

Replace `user` with your username and `remote_host` with the IP address or domain of the remote server.

## Connecting to a Remote Server

To connect to a remote server using SSH:

```sh
ssh user@remote_host
```

Replace `user` with your username and `remote_host` with the IP address or domain of the remote server.

## SSH Configuration File

You can configure SSH options in the `~/.ssh/config` file. Here is an example configuration:

```sh
Host myserver
    HostName remote_host
    User user
    Port 22
    IdentityFile ~/.ssh/id_rsa
```

Replace `myserver`, `remote_host`, `user`, and `~/.ssh/id_rsa` with your own values. This allows you to connect using a simple command:

```sh
ssh myserver
```

## Transferring Files with SCP

To copy a file from your local machine to a remote server:

```sh
scp local_file user@remote_host:/remote_directory
```

To copy a file from a remote server to your local machine:

```sh
scp user@remote_host:/remote_file local_directory
```

Replace `local_file`, `user`, `remote_host`, `/remote_directory`, `/remote_file`, and `local_directory` with your own values.

## Transferring Files with SFTP

To start an SFTP session to a remote server:

```sh
sftp user@remote_host
```

Once connected, you can use commands like `put` to upload files and `get` to download files.

## Tunneling with SSH

To create an SSH tunnel for port forwarding:

```sh
ssh -L local_port:localhost:remote_port user@remote_host
```

Replace `local_port`, `remote_port`, `user`, and `remote_host` with your own values.

## Forwarding SSH Agent

To forward your SSH agent to a remote server:

```sh
ssh -A user@remote_host
```

This allows you to use your local SSH keys on the remote server.

## Managing Known Hosts

The `~/.ssh/known_hosts` file keeps track of remote servers you've connected to. To remove a host's entry:

```sh
ssh-keygen -R remote_host
```

Replace `remote_host` with the IP address or domain of the remote server.

## Disabling SSH Root Login

To disable root login via SSH, edit the SSH configuration file on the remote server (`/etc/ssh/sshd_config`) and set:

```sh
PermitRootLogin no
```

Restart the SSH service to apply the changes.

## Restarting SSH Service

To restart the SSH service on a Debian-based system:

```sh
sudo systemctl restart ssh
```

To restart the SSH service on a Red Hat-based system:

```sh
sudo systemctl restart sshd
```