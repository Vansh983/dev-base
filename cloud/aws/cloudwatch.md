# AWS CLI - CloudWatch Commands

## Overview
- [AWS CLI - CloudWatch Commands](#aws-cli---cloudwatch-commands)
  - [Overview](#overview)
  - [Listing CloudWatch Alarms](#listing-cloudwatch-alarms)
  - [Creating a CloudWatch Alarm](#creating-a-cloudwatch-alarm)
  - [Deleting a CloudWatch Alarm](#deleting-a-cloudwatch-alarm)
  - [Describing CloudWatch Alarm History](#describing-cloudwatch-alarm-history)
  - [Disabling a CloudWatch Alarm](#disabling-a-cloudwatch-alarm)
  - [Enabling a CloudWatch Alarm](#enabling-a-cloudwatch-alarm)
  - [Describing CloudWatch Metrics](#describing-cloudwatch-metrics)
  - [Getting Metric Statistics](#getting-metric-statistics)
  - [Putting Custom Metrics](#putting-custom-metrics)
  - [Creating a Dashboard](#creating-a-dashboard)
  - [Deleting a Dashboard](#deleting-a-dashboard)

## Listing CloudWatch Alarms

To list all CloudWatch alarms.

```sh
aws cloudwatch describe-alarms
```

## Creating a CloudWatch Alarm

To create a new CloudWatch alarm.

```sh
aws cloudwatch put-metric-alarm --alarm-name my-alarm --metric-name CPUUtilization --namespace AWS/EC2 --statistic Average --period 300 --threshold 80 --comparison-operator GreaterThanOrEqualToThreshold --dimensions Name=InstanceId,Value=i-1234567890abcdef0 --evaluation-periods 2 --alarm-actions arn:aws:sns:us-east-1:123456789012:my-sns-topic --unit Percent
```

## Deleting a CloudWatch Alarm

To delete a CloudWatch alarm.

```sh
aws cloudwatch delete-alarms --alarm-names my-alarm
```

## Describing CloudWatch Alarm History

To describe the history of a specific CloudWatch alarm.

```sh
aws cloudwatch describe-alarm-history --alarm-name my-alarm
```

## Disabling a CloudWatch Alarm

To disable a specific CloudWatch alarm.

```sh
aws cloudwatch disable-alarm-actions --alarm-names my-alarm
```

## Enabling a CloudWatch Alarm

To enable a specific CloudWatch alarm.

```sh
aws cloudwatch enable-alarm-actions --alarm-names my-alarm
```

## Describing CloudWatch Metrics

To describe available CloudWatch metrics.

```sh
aws cloudwatch list-metrics
```

## Getting Metric Statistics

To get statistics for a specific metric.

```sh
aws cloudwatch get-metric-statistics --metric-name CPUUtilization --start-time 2023-01-01T00:00:00Z --end-time 2023-01-02T00:00:00Z --period 3600 --namespace AWS/EC2 --statistics Average --dimensions Name=InstanceId,Value=i-1234567890abcdef0
```

## Putting Custom Metrics

To put custom metrics into CloudWatch.

```sh
aws cloudwatch put-metric-data --metric-name MyCustomMetric --namespace MyNamespace --value 1
```

## Creating a Dashboard

To create a CloudWatch dashboard.

```sh
aws cloudwatch put-dashboard --dashboard-name MyDashboard --dashboard-body file://dashboard.json
```

## Deleting a Dashboard

To delete a CloudWatch dashboard.

```sh
aws cloudwatch delete-dashboards --dashboard-names MyDashboard
```