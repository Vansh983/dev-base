# Redis Commands

## Overview
- [Redis Commands](#redis-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing Redis](#installing-redis)
  - [Starting Redis Server](#starting-redis-server)
  - [Stopping Redis Server](#stopping-redis-server)
  - [Connecting to Redis](#connecting-to-redis)
  - [Setting a Key](#setting-a-key)
  - [Getting a Key](#getting-a-key)
  - [Deleting a Key](#deleting-a-key)
  - [Listing All Keys](#listing-all-keys)
  - [Checking Key Existence](#checking-key-existence)
  - [Setting a Key with Expiry](#setting-a-key-with-expiry)
  - [Checking Key TTL](#checking-key-ttl)
  - [Persisting a Key](#persisting-a-key)
  - [Flushing All Data](#flushing-all-data)
  - [Saving Data to Disk](#saving-data-to-disk)
  - [Loading Data from Disk](#loading-data-from-disk)
  - [Monitoring Redis](#monitoring-redis)

## Introduction

Redis is an open-source, in-memory data structure store used as a database, cache, and message broker. It supports data structures such as strings, hashes, lists, sets, and more.

## Installing Redis

To install Redis on macOS using Homebrew:

```sh
brew install redis
```

## Starting Redis Server

To start the Redis server:

```sh
redis-server
```

To start the Redis server using Homebrew services:

```sh
brew services start redis
```

## Stopping Redis Server

To stop the Redis server using Homebrew services:

```sh
brew services stop redis
```

## Connecting to Redis

To connect to the Redis server using the Redis CLI:

```sh
redis-cli
```

## Setting a Key

To set a key in Redis:

```sh
SET key value
```

Replace `key` with the name of your key and `value` with the value you want to store.

## Getting a Key

To get the value of a key:

```sh
GET key
```

Replace `key` with the name of your key.

## Deleting a Key

To delete a key:

```sh
DEL key
```

Replace `key` with the name of your key.

## Listing All Keys

To list all keys in the current database:

```sh
KEYS *
```

## Checking Key Existence

To check if a key exists:

```sh
EXISTS key
```

Replace `key` with the name of your key.

## Setting a Key with Expiry

To set a key with an expiry time (in seconds):

```sh
SETEX key seconds value
```

Replace `key` with the name of your key, `seconds` with the expiry time in seconds, and `value` with the value you want to store.

## Checking Key TTL

To check the time-to-live (TTL) of a key:

```sh
TTL key
```

Replace `key` with the name of your key.

## Persisting a Key

To remove the expiry from a key:

```sh
PERSIST key
```

Replace `key` with the name of your key.

## Flushing All Data

To delete all keys from all databases:

```sh
FLUSHALL
```

To delete all keys from the current database:

```sh
FLUSHDB
```

## Saving Data to Disk

To perform a synchronous save of the dataset to disk:

```sh
SAVE
```

To perform an asynchronous save of the dataset to disk:

```sh
BGSAVE
```

## Loading Data from Disk

Redis loads data from disk automatically when it starts, so no specific command is needed for loading data from disk.

## Monitoring Redis

To monitor the commands processed by the Redis server in real-time:

```sh
MONITOR
```