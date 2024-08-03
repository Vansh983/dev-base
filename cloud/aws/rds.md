# AWS CLI - RDS Commands

## Overview
- [AWS CLI - RDS Commands](#aws-cli---rds-commands)
  - [Overview](#overview)
  - [Listing RDS Instances](#listing-rds-instances)
  - [Starting an RDS Instance](#starting-an-rds-instance)
  - [Stopping an RDS Instance](#stopping-an-rds-instance)
  - [Rebooting an RDS Instance](#rebooting-an-rds-instance)
  - [Deleting an RDS Instance](#deleting-an-rds-instance)
  - [Creating an RDS Snapshot](#creating-an-rds-snapshot)
  - [Deleting an RDS Snapshot](#deleting-an-rds-snapshot)
  - [Restoring an RDS Instance from a Snapshot](#restoring-an-rds-instance-from-a-snapshot)
  - [Modifying an RDS Instance](#modifying-an-rds-instance)
  - [Describing RDS Security Groups](#describing-rds-security-groups)
  - [Creating an RDS Security Group](#creating-an-rds-security-group)
  - [Deleting an RDS Security Group](#deleting-an-rds-security-group)
  - [Adding Ingress Rules to an RDS Security Group](#adding-ingress-rules-to-an-rds-security-group)
  - [Removing Ingress Rules from an RDS Security Group](#removing-ingress-rules-from-an-rds-security-group)

## Listing RDS Instances

To list all RDS instances.

```sh
aws rds describe-db-instances
```

## Starting an RDS Instance

To start an RDS instance.

```sh
aws rds start-db-instance --db-instance-identifier mydbinstance
```

## Stopping an RDS Instance

To stop an RDS instance.

```sh
aws rds stop-db-instance --db-instance-identifier mydbinstance
```

## Rebooting an RDS Instance

To reboot an RDS instance.

```sh
aws rds reboot-db-instance --db-instance-identifier mydbinstance
```

## Deleting an RDS Instance

To delete an RDS instance.

```sh
aws rds delete-db-instance --db-instance-identifier mydbinstance --skip-final-snapshot
```

## Creating an RDS Snapshot

To create a snapshot of an RDS instance.

```sh
aws rds create-db-snapshot --db-snapshot-identifier mydbsnapshot --db-instance-identifier mydbinstance
```

## Deleting an RDS Snapshot

To delete an RDS snapshot.

```sh
aws rds delete-db-snapshot --db-snapshot-identifier mydbsnapshot
```

## Restoring an RDS Instance from a Snapshot

To restore an RDS instance from a snapshot.

```sh
aws rds restore-db-instance-from-db-snapshot --db-instance-identifier mynewdbinstance --db-snapshot-identifier mydbsnapshot
```

## Modifying an RDS Instance

To modify an RDS instance (e.g., changing instance class or storage).

```sh
aws rds modify-db-instance --db-instance-identifier mydbinstance --allocated-storage 100 --db-instance-class db.m5.large --apply-immediately
```

## Describing RDS Security Groups

To describe RDS security groups.

```sh
aws rds describe-db-security-groups
```

## Creating an RDS Security Group

To create a new RDS security group.

```sh
aws rds create-db-security-group --db-security-group-name mysecuritygroup --db-security-group-description "My security group"
```

## Deleting an RDS Security Group

To delete an RDS security group.

```sh
aws rds delete-db-security-group --db-security-group-name mysecuritygroup
```

## Adding Ingress Rules to an RDS Security Group

To add ingress rules to an RDS security group.

```sh
aws rds authorize-db-security-group-ingress --db-security-group-name mysecuritygroup --cidr-ip 203.0.113.0/24
```

## Removing Ingress Rules from an RDS Security Group

To remove ingress rules from an RDS security group.

```sh
aws rds revoke-db-security-group-ingress --db-security-group-name mysecuritygroup --cidr-ip 203.0.113.0/24
```