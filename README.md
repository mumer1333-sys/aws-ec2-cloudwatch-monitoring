# aws-ec2-cloudwatch-monitoring

## What This Project Does
This project sets up a cloud monitoring pipeline on AWS from scratch. An EC2 instance runs as the server, with the CloudWatch Agent installed to collect and stream live CPU, memory, and disk metrics. A CloudWatch alarm monitors CPU usage and triggers when it crosses a set threshold — verified with a live stress test that spiked the CPU and flipped the alarm to "In Alarm" state. IAM roles control permissions throughout, following the principle of least privilege.

## Architecture
Simple diagram or description of what connects to what
EC2 → CloudWatch Agent → CloudWatch Metrics → Alarm → SNS

## Services Used
- EC2 (t3.micro, Amazon Linux)
- IAM (role with CloudWatchAgentServerPolicy + AmazonSSMManagedInstanceCore)
- CloudWatch Agent
- CloudWatch Alarms
- SNS

## What I Learned
- IAM roles and least privilege
- CloudWatch Agent metric collection
- Alarms and thresholds in practice
- SSH troubleshooting
- Temporary vs permanent credentials (ASIA vs AKIA)

## Troubleshooting I Encountered
- AccessDeniedException: missing SSM permission on IAM role
- SSH parse error from angle brackets in command
- Private vs public IP confusion
- SNS notification not attaching to alarm

## Screenshots

## SAA Concepts Covered
- EC2 instance types and families
- IAM roles vs users
- Security groups (stateful)
- CloudWatch metrics, namespaces, and alarms
