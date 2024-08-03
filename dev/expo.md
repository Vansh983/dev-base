# Expo and EAS Commands

## Overview
- [Expo and EAS Commands](#expo-and-eas-commands)
  - [Overview](#overview)
  - [Installing Expo CLI](#installing-expo-cli)
  - [Checking Expo CLI Version](#checking-expo-cli-version)
  - [Creating a New Expo Project](#creating-a-new-expo-project)
  - [Starting the Development Server](#starting-the-development-server)
  - [Publishing a Project](#publishing-a-project)
  - [Building a Project with EAS](#building-a-project-with-eas)
  - [Installing EAS CLI](#installing-eas-cli)
  - [Checking EAS CLI Version](#checking-eas-cli-version)
  - [Configuring EAS Build](#configuring-eas-build)
  - [Running EAS Build](#running-eas-build)
  - [Managing EAS Builds](#managing-eas-builds)
  - [EAS Submit](#eas-submit)

## Installing Expo CLI

To install Expo CLI globally:

```sh
npm install -g expo-cli
```

## Checking Expo CLI Version

To check the version of Expo CLI installed:

```sh
expo --version
```

## Creating a New Expo Project

To create a new Expo project:

```sh
expo init project-name
```

Replace `project-name` with the name of your project.

## Starting the Development Server

To start the development server for your Expo project:

```sh
expo start
```

## Publishing a Project

To publish your Expo project:

```sh
expo publish
```

## Building a Project with EAS

To build your project using EAS, first, install the EAS CLI.

## Installing EAS CLI

To install EAS CLI globally:

```sh
npm install -g eas-cli
```

## Checking EAS CLI Version

To check the version of EAS CLI installed:

```sh
eas --version
```

## Configuring EAS Build

To configure EAS Build for your project, run the following command and follow the prompts:

```sh
eas build:configure
```

This will create an `eas.json` configuration file in your project.

## Running EAS Build

To create a build for your project:

```sh
eas build --platform ios
eas build --platform android
```

You can also build for both platforms:

```sh
eas build --platform all
```

## Managing EAS Builds

To list all your builds:

```sh
eas build:list
```

To get the status of a specific build:

```sh
eas build:view build-id
```

Replace `build-id` with the ID of the build you want to check.

## EAS Submit

To submit your build to the App Store or Google Play:

```sh
eas submit --platform ios
eas submit --platform android
```

Follow the prompts to provide the necessary information for submission.