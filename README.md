# aws-serverless-ec2-scheduler
This project automates the starting and stopping of EC2 instances during business hours using AWS Lambda, IAM, and EventBridge.

## Services Used

| Service          | Purpose                                |
|------------------|----------------------------------------|
| **EC2**          | Virtual machine being managed          |
| **Lambda**       | Executes start/stop logic              |
| **IAM**          | Defines permissions for Lambda         |
| **EventBridge**  | Triggers Lambda functions on schedule  |
| **CloudWatch Logs** | Monitors and logs Lambda execution |

## What It Does

- Starts EC2 instance at 08:00 every weekday
- Stops EC2 instance at 17:00 every weekday
- Uses separate IAM roles and policies for security
- Serverless, cost-efficient automation

<pre> ## Folder Structure ``` . ├── start_instance.py # Lambda for starting EC2 ├── stop_instance.py # Lambda for stopping EC2 ├── iam-policies/ │ ├── start-policy.json # IAM policy for start function │ └── stop-policy.json # IAM policy for stop function ├── cloudwatch-schedule/ │ └── schedule-details.md # Cron schedule details └── README.md # Project documentation ``` </pre>

## How to Use

1. Deploy two Lambda functions with the provided Python files
2. Create IAM roles and attach the corresponding policies
3. Schedule using EventBridge (cron)
4. Monitor via CloudWatch Logs

## IAM Permissions

See `iam-policies` for least-privilege examples.

## Scheduling

See `cloudwatch-schedule` for cron expressions and details.

## Future Improvements

- Tag-based instance filtering
- Multi-instance or multi-region support
- CloudFormation or Terraform automation

---

Created as a learning project to explore AWS automation and serverless best practices.

