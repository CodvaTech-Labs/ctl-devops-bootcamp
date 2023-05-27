+++
title = "Get Access Key and Secret Access Key"
weight = 14
chapter = false
pre = "<b> 1.1 </b>"
+++

To get your AWS Access Key ID and AWS Secret Access Key, you can follow these steps:

1. Sign in to the AWS Management Console: Open your web browser and go to the AWS Management Console at https://console.aws.amazon.com/. Sign in using your AWS account credentials.

2. Open the IAM service: Once you are logged in to the AWS Management Console, search for "IAM" (Identity and Access Management) in the services search bar, and click on the IAM service to open it.

3. Access the Users section: In the IAM console, locate the "Users" option in the left navigation pane and click on it. This will show you a list of IAM users in your AWS account.

4. Create a new IAM user (optional): If you don't have an existing IAM user with the necessary permissions, you can create a new IAM user by clicking on the "Add user" button. Follow the instructions to provide a username and set the access type.

5. Generate access keys: In the list of IAM users, locate the user for which you want to generate the access keys and click on the username to access the user's details.

6. Access the Security Credentials tab: Within the user's details, navigate to the "Security credentials" tab, which provides access to the user's security-related settings.

7. Create access keys: Under the "Access keys" section, click on the "Create access key" button. This will generate a new access key pair for the selected IAM user.

8. Copy the Access Key ID and Secret Access Key: Once the access keys are generated, you will see the Access Key ID and Secret Access Key on the screen. Copy these values or download the CSV file that contains the access key details.

Important: The Secret Access Key is only displayed once when the keys are first generated. Make sure to securely store the Secret Access Key in a safe location. If you lose it, you will need to generate a new access key pair.

That's it! You now have your AWS Access Key ID and AWS Secret Access Key. These credentials are essential for configuring AWS CLI or any other AWS service that requires access to your AWS account.