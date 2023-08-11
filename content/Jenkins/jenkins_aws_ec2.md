+++
title = "Jenkins Use Case "
weight = 27
chapter = false
pre = "<b> 2.2 </b>"
+++

## Use Case : Stop | Start AWS EC2 using Jenkins

To stop and start an EC2 instance using a Jenkins Freestyle job, you can utilize the AWS Command Line Interface (AWS CLI) along with shell commands in your Jenkins job configuration. Here's how you can achieve this:

1. **Install AWS CLI on Jenkins Server:**
   If the AWS CLI is not already installed on your Jenkins server, you'll need to install it. You can follow the official AWS CLI installation guide for your specific operating system: [Installing the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

```
yum install aws-cli
aws --version

```

2. **Configure AWS Credentials:**
- Create New IAM Role with EC2 Admistrative Permission
- Attach newly created role to Jenkins Server

3. **Create a Jenkins Freestyle Job:**
   - Log in to your Jenkins instance.
   - Click "New Item" to create a new Freestyle project.
   - Give the job a name and select the appropriate configuration options.

4. **Configure Build Steps:**
   - Under the "Build" section, add build steps to execute AWS CLI commands.
   - Use shell commands to run AWS CLI commands for stopping and starting instances.

5. **Add Shell Commands for Stopping and Starting EC2 Instances:**
   - For stopping an instance:
     ```bash
     # Replace INSTANCE_ID with the actual instance ID
     aws ec2 stop-instances --instance-ids INSTANCE_ID
     ```
   - For starting an instance:
     ```bash
     # Replace INSTANCE_ID with the actual instance ID
     aws ec2 start-instances --instance-ids INSTANCE_ID
     ```

6. **Save the Job Configuration:**
   - After configuring the build steps, click "Save" to save the job configuration.

7. **Run the Jenkins Job:**
   - Once the job is saved, you can manually trigger it by clicking "Build Now."
   - The job will execute the shell commands to stop or start the specified EC2 instance.

Make sure to replace `INSTANCE_ID` with the actual instance ID you want to stop or start.
