+++
title = "Jenkins Installation "
weight = 17
chapter = false
pre = "<b> 1.2 </b>"
+++


Installing Jenkins on an AWS Linux 2 machine involves a few steps, including setting up a Java runtime environment, adding the Jenkins repository, installing Jenkins, and starting the Jenkins service. Here's a step-by-step guide:

**1. Connect to Your AWS Linux 2 Instance:**
   Use SSH to connect to your AWS Linux 2 instance using the terminal.

**2. Update the System:**
   Before proceeding, update the package repositories and installed packages:
   
   ```bash
   sudo yum update
   ```

**3. Install Java:**
   Jenkins requires Java to run. Install Java OpenJDK 8 or 11. For example, to install OpenJDK 8:
   
   ```bash
   sudo yum remove java-1.7.0-openjdk
   sudo amazon-linux-extras install java-openjdk11
   ```

**4. Add Jenkins Repository:**
   Import the Jenkins repository's GPG key and add the Jenkins repository:
   
   ```bash
   sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo

   sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

   sudo amazon-linux-extras install epel -y
   ```

**5. Install Jenkins:**
   Install Jenkins using `yum`:
   
   ```bash
   sudo yum install jenkins
   ```

**6. Start Jenkins:**
   Start the Jenkins service and enable it to start on boot:
   
   ```bash
   sudo systemctl start jenkins
   sudo systemctl enable jenkins
   sudo systemctl status jenkins
   ```

**7. Open Firewall Ports:**
   If you're using a firewall (such as firewalld), open the necessary ports to allow access to Jenkins. For example, to allow HTTP traffic on port 8080:
   
   ```bash
   sudo firewall-cmd --add-port=8080/tcp --permanent
   sudo firewall-cmd --reload
   ```

**8. Access Jenkins Web UI:**
   Jenkins web UI is accessible at `http://your-instance-ip:8080`. Replace `your-instance-ip` with the actual IP address of your AWS instance.

   To retrieve the initial Jenkins admin password, use the following command:
   
   ```bash
   sudo cat /var/lib/jenkins/secrets/initialAdminPassword
   ```

   Copy the password and paste it in the Jenkins web UI to complete the setup.

**9. Install Plugins:**
   Follow the on-screen instructions to install recommended plugins. You can choose the "Install suggested plugins" option during the initial setup.

**10. Customize Jenkins:**
   You can further customize Jenkins as needed, including creating users, setting up security, and configuring your Jenkins environment.

Congratulations, you've successfully installed Jenkins on your AWS Linux 2 machine. You can now start creating pipelines, jobs, and automation for your CI/CD workflows.