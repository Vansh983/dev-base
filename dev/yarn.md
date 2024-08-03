# Yarn Commands

## Overview
- [Yarn Commands](#yarn-commands)
  - [Overview](#overview)
  - [Installing Yarn](#installing-yarn)
  - [Checking Yarn Version](#checking-yarn-version)
  - [Initializing a New Project](#initializing-a-new-project)
  - [Adding a Dependency](#adding-a-dependency)
  - [Removing a Dependency](#removing-a-dependency)
  - [Installing Dependencies](#installing-dependencies)
  - [Upgrading a Dependency](#upgrading-a-dependency)
  - [Running Scripts](#running-scripts)
  - [Listing Installed Packages](#listing-installed-packages)
  - [Cleaning the Cache](#cleaning-the-cache)
  - [Generating a Lockfile](#generating-a-lockfile)

## Installing Yarn

To install Yarn on macOS using Homebrew:

```sh
brew install yarn
```

## Checking Yarn Version

To check the version of Yarn installed:

```sh
yarn --version
```

## Initializing a New Project

To initialize a new Yarn project:

```sh
yarn init
```

This command will prompt you to enter details about your project.

## Adding a Dependency

To add a dependency to your project:

```sh
yarn add package-name
```

Replace `package-name` with the name of the dependency you want to add.

To add a dependency to a specific category (e.g., `devDependencies`):

```sh
yarn add package-name --dev
```

## Removing a Dependency

To remove a dependency from your project:

```sh
yarn remove package-name
```

Replace `package-name` with the name of the dependency you want to remove.

## Installing Dependencies

To install all dependencies listed in `package.json`:

```sh
yarn install
```

## Upgrading a Dependency

To upgrade a dependency to the latest version:

```sh
yarn upgrade package-name
```

Replace `package-name` with the name of the dependency you want to upgrade.

## Running Scripts

To run a script defined in your `package.json`:

```sh
yarn run script-name
```

Replace `script-name` with the name of the script you want to run.

## Listing Installed Packages

To list all installed packages:

```sh
yarn list
```

## Cleaning the Cache

To clear Yarn's global cache:

```sh
yarn cache clean
```

## Generating a Lockfile

To generate a lockfile:

```sh
yarn install --frozen-lockfile
```

This ensures that the exact versions in your `yarn.lock` file are installed.