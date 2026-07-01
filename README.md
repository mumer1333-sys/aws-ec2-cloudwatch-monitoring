# aws-ec2-cloudwatch-monitoring

## What This Project Does
Brief 2-3 sentence summary

## Architecture
Simple diagram or description of what connects to what
EC2 → CloudWatch Agent → CloudWatch Metrics → Alarm → SNS

## Services Used
- EC2 (t3.micro, Amazon Linux 2023)
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
