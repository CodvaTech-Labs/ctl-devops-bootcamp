+++
title = "Configure AWS CLI - Mac OS"
weight = 6
chapter = false
pre = "<b> 1.2 </b>"
+++

## Setup AWS CLI
To set up the AWS Command Line Interface (CLI) on a MacBook, you can follow these steps:

1. Install Python: AWS CLI requires Python to be installed on your MacBook. By default, macOS comes with a pre-installed version of Python. Open the Terminal application (you can find it in the "Utilities" folder within "Applications") and run the following command to check if Python is installed:

```sh
python --version
```
If Python is not installed, you can download and install it from the official Python website (https://www.python.org/downloads/). It is recommended to install the latest stable version.

2. Install AWS CLI using pip: In the Terminal, run the following command to install AWS CLI using the Python package manager, pip:
```sh
pip install awscli --upgrade --user
```
This command will download and install the AWS CLI and its dependencies. The `--upgrade` flag ensures that you get the latest version of AWS CLI, and the `--user` flag installs it in the user's directory.

3. Verify AWS CLI installation: After the installation is complete, you can verify if AWS CLI is installed correctly by running the following command in the Terminal:
```sh
aws --version
```
If the installation was successful, it will display the version of AWS CLI installed on your system.

4. Configure AWS CLI: To use AWS CLI, you need to configure it with your AWS credentials. Run the following command in the Terminal:

```sh
aws configure
```

This command will prompt you to enter your AWS Access Key ID, AWS Secret Access Key, default region, and default output format. You can obtain the Access Key ID and Secret Access Key from the AWS Management Console. The default region is the AWS region you want to interact with (e.g., "us-west-2" for US West (Oregon)). The default output format can be set to "json" or "text".

Once you have entered the required information, it will be stored in a configuration file on your system.

5. Validate AWS CLI installation using below command
```sh
aws s3 ls
```
That's it! You have successfully set up AWS CLI on your MacBook. You can now use AWS CLI commands to interact with various AWS services from the Terminal.



