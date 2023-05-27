+++
title = "Configure AWS CLI - Windows"
weight = 5
chapter = false
pre = "<b> 1.1 </b>"
+++

## Setup AWS CLI
Follow below steps for installation of AWS CLI on Windows Operating System

- Verify Python installation: AWS CLI requires Python to be installed on your Windows laptop. Open the Command Prompt by searching for "Command Prompt" in the Windows Start menu. 

- Then, type the following command and press Enter to check if Python is installed:

```sh
python --version
```
- If Python is not installed, download and install the latest version of Python from the official website (https://www.python.org/downloads/). Make sure to select the option to add Python to the system PATH during the installation process.

- Open the Command Prompt: Open the Command Prompt on your Windows laptop. You can do this by searching for "Command Prompt" in the Windows Start menu.
- Install AWS CLI using pip: In the Command Prompt, run the following command to install AWS CLI using the Python package manager, pip:

```sh
pip install awscli
```

- This command will download and install the AWS CLI and its dependencies.

- Verify AWS CLI installation: After the installation is complete, you can verify if AWS CLI is installed correctly by running the following command in the Command Prompt:

```sh
aws --version

```

- If the installation was successful, it will display the version of AWS CLI installed on your system.

- Configure AWS CLI: To use AWS CLI, you need to configure it with your AWS credentials. Run the following command in the Command Prompt:

```sh
aws configure
```

- This command will prompt you to enter your AWS Access Key ID, AWS Secret Access Key, default region, and default output format. You can obtain the Access Key ID and Secret Access Key from the AWS Management Console. The default region is the AWS region you want to interact with (e.g., "us-west-2" for US West (Oregon)). The default output format can be set to "json" or "text".

- Ref this link to get IAM User Access Key and Secret Access Key (http://localhost:56450/aws/iam/iam_keys/)

- Once you have entered the required information, it will be stored in a configuration file on your system.

- That's it! You have successfully installed and configured AWS CLI on your Windows laptop. 

- Validate AWS CLI installation using below command
```sh
aws s3 ls
```

- You can now use AWS CLI commands to interact with various AWS services from the Command Promp



