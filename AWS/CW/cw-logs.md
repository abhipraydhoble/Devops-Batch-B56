## create policy with following permission
````
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "cloudwatch:PutMetricData",
        "ec2:DescribeTags",
        "ec2:DescribeInstances",
        "logs:PutLogEvents",
        "logs:CreateLogGroup",
        "logs:CreateLogStream"
      ],
      "Resource": "*"
    }
  ]
}
````
## create role and attach policy


## install cloudwatch agent
````
sudo yum install  amazon-cloudwatch-agent -y
````



## vim config.json 

````
sudo vim /opt/aws/amazon-cloudwatch-agent/etc/config.json
````
## copy below script in config.json file
````
{
  "logs": {
    "logs_collected": {
      "files": {
        "collect_list": [
          {
            "file_path": "/var/log/messages",
            "log_group_name": "test-lambda-function",
            "log_stream_name": "{instance_id}/messages",
            "timestamp_format": "%b %d %H:%M:%S"
          },
          {
            "file_path": "/var/log/test.log",
            "log_group_name": "test-lambda-function",
            "log_stream_name": "{instance_id}/test-log",
            "timestamp_format": "%Y-%m-%d %H:%M:%S"
          }
        ]
      }
    }
  }
}

````
## start cloudwatch agent
````
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl \
  -a fetch-config -m ec2 \
  -c file:/opt/aws/amazon-cloudwatch-agent/etc/config.json \
  -s

````
## check status
````
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -m ec2 -a status

````
## generate logs
````
#!/bin/bash

LOG_FILE="/var/log/test.log"

while true; do
  echo "$(date '+%Y-%m-%d %H:%M:%S') - This is a test log line." >> "$LOG_FILE"
  sleep 5
done

````
````
sudo chmod +x log.sh
````

````
sudo ./log.sh
````


