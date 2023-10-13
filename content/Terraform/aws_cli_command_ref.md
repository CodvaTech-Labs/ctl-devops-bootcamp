+++
title = "AWS CLI Commands"
weight = 10
chapter = false
pre = "<b> 1.7 </b>"
+++


### AWS CLI Commands : 

Certainly, here are the AWS CLI commands for the tasks you mentioned:

1. **Stop EC2 Instance:**

```sh
aws ec2 stop-instances --instance-ids <your-instance-id>
```

2. **Start EC2 Instance:**

```sh
aws ec2 start-instances --instance-ids <your-instance-id>
```

3. **Terminate EC2 Instance:**

```sh
aws ec2 terminate-instances --instance-ids <your-instance-id>
```

4. **Restart EC2 Instance (Stop and Start):**

```sh
aws ec2 stop-instances --instance-ids <your-instance-id> && aws ec2 start-instances --instance-ids <your-instance-id>
```

5. **Create a Snapshot (Backup) of an EC2 EBS Volume:**

```sh
aws ec2 create-snapshot --volume-id <your-volume-id> --description "Your snapshot description"
```

Replace `<your-volume-id>` with the actual volume ID of the EBS volume you want to create a snapshot of.

6. **Create an AMI (Amazon Machine Image) from an EC2 Instance:**

```sh
aws ec2 create-image --instance-id <your-instance-id> --name "Your AMI Name" --description "Your AMI description"
```

Replace `<your-instance-id>` with the instance ID of the EC2 instance you want to create an AMI from.

7. **Delete a Backup (Snapshot) by Snapshot ID:**

```sh
aws ec2 delete-snapshot --snapshot-id <your-snapshot-id>
```

Replace `<your-snapshot-id>` with the actual snapshot ID you want to delete.


9. **Create a New EC2 Instance:**

You can create a new EC2 instance using the `run-instances` command. Here's a basic example:

```sh
aws ec2 run-instances --image-id <ami-id> --instance-type <instance-type> --key-name <key-pair-name>
```

Replace `<ami-id>`, `<instance-type>`, and `<key-pair-name>` with the appropriate values for your new instance.

These commands will help you perform the specified tasks using the AWS CLI. Make sure to replace placeholders with actual IDs and values.