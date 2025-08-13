# EventBridge Schedule

- **Start Rule:** Runs daily at 08:00 (UTC+10)
- **Stop Rule:** Runs daily at 17:00 (UTC+10)

Both rules trigger the respective Lambda functions via cron expressions:

- Start: `cron(0 22 ? * MON-FRI *)`
- Stop: `cron(0 7 ? * MON-FRI *)`
