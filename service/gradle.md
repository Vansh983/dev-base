# Gradle Commands

## Overview
- [Gradle Commands](#gradle-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing Gradle](#installing-gradle)
  - [Checking Gradle Version](#checking-gradle-version)
  - [Creating a New Gradle Project](#creating-a-new-gradle-project)
  - [Building a Project](#building-a-project)
  - [Running Tests](#running-tests)
  - [Running a Project](#running-a-project)
  - [Cleaning a Project](#cleaning-a-project)
  - [Listing Tasks](#listing-tasks)
  - [Running a Specific Task](#running-a-specific-task)
  - [Adding Dependencies](#adding-dependencies)
  - [Using the Gradle Wrapper](#using-the-gradle-wrapper)
  - [Generating a Gradle Wrapper](#generating-a-gradle-wrapper)
  - [Viewing Dependency Tree](#viewing-dependency-tree)
  - [Updating Dependencies](#updating-dependencies)

## Introduction

Gradle is an open-source build automation tool focused on flexibility and performance. It is used for building, testing, and deploying software projects.

## Installing Gradle

To install Gradle on macOS using Homebrew:

```sh
brew install gradle
```

## Checking Gradle Version

To check the version of Gradle installed:

```sh
gradle --version
```

## Creating a New Gradle Project

To create a new Gradle project:

```sh
gradle init
```

Follow the prompts to set up your project.

## Building a Project

To build your project:

```sh
gradle build
```

## Running Tests

To run tests in your project:

```sh
gradle test
```

## Running a Project

To run your project:

```sh
gradle run
```

Ensure that you have an application plugin applied and a `mainClassName` configured.

## Cleaning a Project

To clean your project (remove build directory):

```sh
gradle clean
```

## Listing Tasks

To list all available tasks in your project:

```sh
gradle tasks
```

## Running a Specific Task

To run a specific task:

```sh
gradle task-name
```

Replace `task-name` with the name of the task you want to run.

## Adding Dependencies

To add dependencies to your project, edit the `build.gradle` file:

```groovy
dependencies {
    implementation 'group:name:version'
}
```

Replace `group:name:version` with the dependency coordinates.

## Using the Gradle Wrapper

To use the Gradle Wrapper, run the following command to execute Gradle tasks:

```sh
./gradlew task-name
```

Replace `task-name` with the name of the task you want to run.

## Generating a Gradle Wrapper

To generate a Gradle Wrapper for your project:

```sh
gradle wrapper
```

This will create the necessary wrapper files in your project.

## Viewing Dependency Tree

To view the dependency tree for your project:

```sh
gradle dependencies
```

## Updating Dependencies

To update dependencies, you can use the `refresh-dependencies` task:

```sh
gradle build --refresh-dependencies
```