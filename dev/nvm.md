# NVM Commands

## Overview
- [NVM Commands](#nvm-commands)
  - [Overview](#overview)
  - [Installing NVM](#installing-nvm)
  - [Checking NVM Version](#checking-nvm-version)
  - [Listing Installed Node Versions](#listing-installed-node-versions)
  - [Installing a Specific Node Version](#installing-a-specific-node-version)
  - [Using a Specific Node Version](#using-a-specific-node-version)
  - [Setting a Default Node Version](#setting-a-default-node-version)
  - [Uninstalling a Node Version](#uninstalling-a-node-version)
  - [Updating NVM](#updating-nvm)
  - [Listing NVM Commands](#listing-nvm-commands)

## Installing NVM

To install NVM, run the following command in your terminal:

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash
```

Then, add the following lines to your `~/.zshrc` or `~/.bash_profile` file:

```sh
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

After adding these lines, reload your terminal configuration:

```sh
source ~/.zshrc  # For zsh
source ~/.bash_profile  # For bash
```

## Checking NVM Version

To check the version of NVM installed:

```sh
nvm --version
```

## Listing Installed Node Versions

To list all installed Node.js versions:

```sh
nvm ls
```

## Installing a Specific Node Version

To install a specific version of Node.js:

```sh
nvm install node-version
```

Replace `node-version` with the version number you want to install, for example, `nvm install 14.17.0`.

## Using a Specific Node Version

To switch to a specific version of Node.js:

```sh
nvm use node-version
```

Replace `node-version` with the version number you want to use, for example, `nvm use 14.17.0`.

## Setting a Default Node Version

To set a default Node.js version to be used in any new shell:

```sh
nvm alias default node-version
```

Replace `node-version` with the version number you want to set as default, for example, `nvm alias default 14.17.0`.

## Uninstalling a Node Version

To uninstall a specific version of Node.js:

```sh
nvm uninstall node-version
```

Replace `node-version` with the version number you want to uninstall, for example, `nvm uninstall 14.17.0`.

## Updating NVM

To update NVM to the latest version:

```sh
nvm install-latest-npm
```

## Listing NVM Commands

To list all available NVM commands:

```sh
nvm help
```