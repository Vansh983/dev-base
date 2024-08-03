# GCP Commands

## Overview
- [GCP Commands](#gcp-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing gcloud CLI](#installing-gcloud-cli)
  - [Initializing gcloud CLI](#initializing-gcloud-cli)
  - [Configuring gcloud CLI](#configuring-gcloud-cli)
  - [Listing Projects](#listing-projects)
  - [Setting Default Project](#setting-default-project)
  - [Creating a New Project](#creating-a-new-project)
  - [Authenticating with gcloud CLI](#authenticating-with-gcloud-cli)
  - [Managing Compute Engine Instances](#managing-compute-engine-instances)
  - [Managing Cloud Storage Buckets](#managing-cloud-storage-buckets)
  - [Deploying to App Engine](#deploying-to-app-engine)
  - [Managing Kubernetes Clusters](#managing-kubernetes-clusters)
  - [Viewing Logs](#viewing-logs)
  - [Billing and Account Management](#billing-and-account-management)

## Introduction

Google Cloud Platform (GCP) is a suite of cloud computing services that runs on the same infrastructure that Google uses internally for its end-user products. GCP offers a range of services including computing, storage, and machine learning.

## Installing gcloud CLI

To install the gcloud CLI, follow the instructions on the [official Google Cloud documentation](https://cloud.google.com/sdk/docs/install).

## Initializing gcloud CLI

To initialize the gcloud CLI:

```sh
gcloud init
```

Follow the prompts to configure your gcloud settings.

## Configuring gcloud CLI

To configure your gcloud CLI with a specific configuration:

```sh
gcloud config configurations create my-config
gcloud config set project my-project
gcloud config set compute/region my-region
gcloud config set compute/zone my-zone
```

Replace `my-config`, `my-project`, `my-region`, and `my-zone` with your own values.

## Listing Projects

To list all projects associated with your account:

```sh
gcloud projects list
```

## Setting Default Project

To set the default project for gcloud:

```sh
gcloud config set project my-project
```

Replace `my-project` with your project ID.

## Creating a New Project

To create a new project in GCP:

```sh
gcloud projects create my-new-project --set-as-default
```

Replace `my-new-project` with your desired project ID.

## Authenticating with gcloud CLI

To authenticate the gcloud CLI with your Google account:

```sh
gcloud auth login
```

To authenticate a service account with a key file:

```sh
gcloud auth activate-service-account --key-file=path/to/key-file.json
```

Replace `path/to/key-file.json` with the path to your service account key file.

## Managing Compute Engine Instances

To list all Compute Engine instances:

```sh
gcloud compute instances list
```

To start a Compute Engine instance:

```sh
gcloud compute instances start instance-name --zone=zone-name
```

To stop a Compute Engine instance:

```sh
gcloud compute instances stop instance-name --zone=zone-name
```

To create a new Compute Engine instance:

```sh
gcloud compute instances create instance-name --zone=zone-name --machine-type=machine-type --image-family=image-family --image-project=image-project
```

Replace `instance-name`, `zone-name`, `machine-type`, `image-family`, and `image-project` with your own values.

## Managing Cloud Storage Buckets

To list all Cloud Storage buckets:

```sh
gsutil ls
```

To create a new Cloud Storage bucket:

```sh
gsutil mb gs://my-bucket
```

To upload a file to a Cloud Storage bucket:

```sh
gsutil cp local-file-path gs://my-bucket
```

To download a file from a Cloud Storage bucket:

```sh
gsutil cp gs://my-bucket/file-name local-file-path
```

Replace `my-bucket`, `local-file-path`, and `file-name` with your own values.

## Deploying to App Engine

To deploy an application to Google App Engine:

```sh
gcloud app deploy
```

## Managing Kubernetes Clusters

To list all Kubernetes clusters:

```sh
gcloud container clusters list
```

To create a new Kubernetes cluster:

```sh
gcloud container clusters create cluster-name --zone=zone-name --num-nodes=3
```

To get credentials for a Kubernetes cluster:

```sh
gcloud container clusters get-credentials cluster-name --zone=zone-name
```

Replace `cluster-name` and `zone-name` with your own values.

## Viewing Logs

To view logs in Google Cloud Logging:

```sh
gcloud logging read "logName=projects/my-project/logs/my-log"
```

Replace `my-project` and `my-log` with your own values.

## Billing and Account Management

To list billing accounts:

```sh
gcloud beta billing accounts list
```

To link a project to a billing account:

```sh
gcloud beta billing projects link my-project --billing-account=my-billing-account
```

Replace `my-project` and `my-billing-account` with your own values.