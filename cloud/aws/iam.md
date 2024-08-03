# AWS CLI - IAM Commands

## Overview
- [AWS CLI - IAM Commands](#aws-cli---iam-commands)
  - [Overview](#overview)
  - [Listing IAM Users](#listing-iam-users)
  - [Creating an IAM User](#creating-an-iam-user)
  - [Deleting an IAM User](#deleting-an-iam-user)
  - [Creating an IAM Group](#creating-an-iam-group)
  - [Deleting an IAM Group](#deleting-an-iam-group)
  - [Adding a User to a Group](#adding-a-user-to-a-group)
  - [Removing a User from a Group](#removing-a-user-from-a-group)
  - [Attaching a Policy to an IAM User](#attaching-a-policy-to-an-iam-user)
  - [Detaching a Policy from an IAM User](#detaching-a-policy-from-an-iam-user)
  - [Attaching a Policy to a Group](#attaching-a-policy-to-a-group)
  - [Detaching a Policy from a Group](#detaching-a-policy-from-a-group)
  - [Creating an IAM Role](#creating-an-iam-role)
  - [Deleting an IAM Role](#deleting-an-iam-role)
  - [Attaching a Policy to a Role](#attaching-a-policy-to-a-role)
  - [Detaching a Policy from a Role](#detaching-a-policy-from-a-role)

## Listing IAM Users

To list all IAM users.

```sh
aws iam list-users
```

## Creating an IAM User

To create a new IAM user.

```sh
aws iam create-user --user-name my-new-user
```

## Deleting an IAM User

To delete an IAM user.

```sh
aws iam delete-user --user-name my-new-user
```

## Creating an IAM Group

To create a new IAM group.

```sh
aws iam create-group --group-name my-new-group
```

## Deleting an IAM Group

To delete an IAM group.

```sh
aws iam delete-group --group-name my-new-group
```

## Adding a User to a Group

To add a user to a group.

```sh
aws iam add-user-to-group --user-name my-user --group-name my-group
```

## Removing a User from a Group

To remove a user from a group.

```sh
aws iam remove-user-from-group --user-name my-user --group-name my-group
```

## Attaching a Policy to an IAM User

To attach a policy to an IAM user.

```sh
aws iam attach-user-policy --user-name my-user --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```

## Detaching a Policy from an IAM User

To detach a policy from an IAM user.

```sh
aws iam detach-user-policy --user-name my-user --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```

## Attaching a Policy to a Group

To attach a policy to a group.

```sh
aws iam attach-group-policy --group-name my-group --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```

## Detaching a Policy from a Group

To detach a policy from a group.

```sh
aws iam detach-group-policy --group-name my-group --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```

## Creating an IAM Role

To create a new IAM role.

```sh
aws iam create-role --role-name my-role --assume-role-policy-document file://policy.json
```

## Deleting an IAM Role

To delete an IAM role.

```sh
aws iam delete-role --role-name my-role
```

## Attaching a Policy to a Role

To attach a policy to a role.

```sh
aws iam attach-role-policy --role-name my-role --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```

## Detaching a Policy from a Role

To detach a policy from a role.

```sh
aws iam detach-role-policy --role-name my-role --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```