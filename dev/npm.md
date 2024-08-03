# Node.js Commands for macOS

## Overview
- [Node.js Commands for macOS](#nodejs-commands-for-macos)
  - [Overview](#overview)
  - [Installing Node.js](#installing-nodejs)
  - [Checking Node.js Version](#checking-nodejs-version)
  - [Running a Node.js Script](#running-a-nodejs-script)
  - [Installing Global Packages](#installing-global-packages)
  - [Installing Local Packages](#installing-local-packages)
  - [Updating Global Packages](#updating-global-packages)
  - [Uninstalling Global Packages](#uninstalling-global-packages)
  - [Listing Installed Global Packages](#listing-installed-global-packages)
  - [Initializing a New Project](#initializing-a-new-project)
  - [Running a Script from package.json](#running-a-script-from-packagejson)

## Installing Node.js

To install Node.js on macOS using Homebrew:

```sh
brew install node
```

## Checking Node.js Version

To check the version of Node.js installed:

```sh
node --version
```

To check the version of npm (Node Package Manager) installed:

```sh
npm --version
```

## Running a Node.js Script

To run a Node.js script:

```sh
node script-name.js
```

Replace `script-name.js` with the name of your Node.js script.

## Installing Global Packages

To install a package globally:

```sh
npm install -g package-name
```

Replace `package-name` with the name of the package you want to install.

## Installing Local Packages

To install a package locally in your project:

```sh
npm install package-name
```

Replace `package-name` with the name of the package you want to install.

## Updating Global Packages

To update a global package:

```sh
npm update -g package-name
```

Replace `package-name` with the name of the package you want to update.

## Uninstalling Global Packages

To uninstall a global package:

```sh
npm uninstall -g package-name
```

Replace `package-name` with the name of the package you want to uninstall.

## Listing Installed Global Packages

To list all installed global packages:

```sh
npm list -g --depth=0
```

## Initializing a New Project

To initialize a new Node.js project and create a `package.json` file:

```sh
npm init
```

This command will prompt you to enter details about your project.

To quickly initialize a new project with default settings:

```sh
npm init -y
```

## Running a Script from package.json

To run a script defined in your `package.json` file:

```sh
npm run script-name
```

Replace `script-name` with the name of the script you want to run.