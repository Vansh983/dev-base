# Prisma Commands

## Overview
- [Prisma Commands](#prisma-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing Prisma](#installing-prisma)
  - [Initializing Prisma](#initializing-prisma)
  - [Generating Prisma Client](#generating-prisma-client)
  - [Deploying Prisma Migrations](#deploying-prisma-migrations)
  - [Resetting the Database](#resetting-the-database)
  - [Running Prisma Studio](#running-prisma-studio)
  - [Creating a Migration](#creating-a-migration)
  - [Applying a Migration](#applying-a-migration)
  - [Rolling Back a Migration](#rolling-back-a-migration)
  - [Seeding the Database](#seeding-the-database)
  - [Checking Prisma Version](#checking-prisma-version)
  - [Previewing a Migration](#previewing-a-migration)

## Introduction

Prisma is an open-source ORM (Object-Relational Mapping) tool for Node.js and TypeScript. It helps developers build and manage databases more effectively by providing a type-safe database client and a set of tools for database schema migrations and management.

## Installing Prisma

To install Prisma CLI globally:

```sh
npm install -g prisma
```

To add Prisma as a dependency in your project:

```sh
npm install @prisma/client
```

## Initializing Prisma

To initialize Prisma in your project:

```sh
prisma init
```

This will create a `prisma` directory with a `schema.prisma` file.

## Generating Prisma Client

To generate the Prisma Client based on your schema:

```sh
prisma generate
```

## Deploying Prisma Migrations

To deploy all pending migrations:

```sh
prisma migrate deploy
```

## Resetting the Database

To reset the database and apply all migrations:

```sh
prisma migrate reset
```

## Running Prisma Studio

To run Prisma Studio, a GUI for viewing and editing your data:

```sh
prisma studio
```

## Creating a Migration

To create a new migration:

```sh
prisma migrate dev --name migration-name
```

Replace `migration-name` with a descriptive name for your migration.

## Applying a Migration

To apply a specific migration:

```sh
prisma migrate deploy
```

## Rolling Back a Migration

To roll back the last migration:

```sh
prisma migrate reset
```

Follow the prompts to reset the database to the state before the last migration.

## Seeding the Database

To seed the database with initial data:

1. Create a `seed.js` or `seed.ts` file in your `prisma` directory.
2. Add the seeding script to your `package.json`:

```json
"prisma": {
  "seed": "node prisma/seed.js"
}
```

3. Run the seed script:

```sh
prisma db seed
```

## Checking Prisma Version

To check the version of Prisma CLI installed:

```sh
prisma --version
```

## Previewing a Migration

To preview what changes a migration will make to the database:

```sh
prisma migrate dev --preview-feature
```

This command will show the SQL that will be executed without applying the migration.
