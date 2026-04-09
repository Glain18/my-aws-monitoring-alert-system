# AWS Monitoring & Alerting System

## Project Overview
This project demonstrates how to monitor an AWS Lambda function using Amazon CloudWatch and send alert notifications through Amazon SNS.

The goal of the project is to detect failures automatically, trigger an alarm, and notify the user by email.

## Architecture
AWS Lambda → CloudWatch Metrics/Logs → CloudWatch Alarm → SNS Topic → Email Notification

## Services Used
- AWS Lambda
- Amazon CloudWatch
- Amazon SNS

## Project Objectives
This project was built to achieve the following:
- Enable CloudWatch logs and metrics for a Lambda function
- Configure at least one CloudWatch alarm
- Send alerts through SNS email notification
- Simulate a failure and verify that the alert is triggered
- Optionally create a dashboard for monitoring

## How It Works
1. A Lambda function is created with code that intentionally raises an exception.
2. Each failed invocation sends logs and error metrics to CloudWatch.
3. A CloudWatch alarm monitors the Errors metric for the Lambda function.
4. When the error threshold is reached, the alarm changes from OK to ALARM.
5. The alarm sends a notification to an SNS topic.
6. SNS sends an email alert to the subscribed email address.

## Lambda Function
The Lambda function used in this project intentionally fails in order to simulate an error condition.

## Evidence
Screenshots for this project are included in the screenshots folder:
 • Lambda test result showing failure
 • CloudWatch alarm in ALARM state
 • SNS email notification
 • CloudWatch dashboard

## Project Outcome

This project successfully demonstrates a basic AWS monitoring and alerting workflow using serverless services. It shows how production issues can be detected automatically and communicated in real time.
