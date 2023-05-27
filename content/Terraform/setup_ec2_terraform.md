+++
title = "Terraform Setup EC2 Instance"
weight = 9
chapter = false
pre = "<b> 1.5 </b>"
+++


### Problem Statement : Setup EC2 instance using Terraform with below specifications.

```sh
Region : Mumbai
Subnet ID : subnet-6f19ee04 (AZ Name : ap-south-1a)
Key Name : devops2022.pem
Security Group : allow http port(Port -80) to everyone (0.0.0.0/0)
```

- User Data: 

```sh
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd.service
systemctl enable httpd.service
echo "Welcome to Terraform Demo!!!, I am $(hostname -f) hosted by Terraform" > /var/www/html/index.html
```

- Create first terraform code in VS Code as below 
```sh
provider "aws" {
  region = "ap-south-1"
}

resource "aws_instance" "ec2_demo" {
  ami           = "ami-079b5e5b3971bd10d"
  instance_type = "t2.micro"
  tags = {
    Name = "Created_By_Terraform"
  }
}
```

- Initiliaze terraform directory using below command 

```sh
terraform init
```

- terraform plan - Execute terraform plan 

```sh
terraform plan
```

- terraform apply - Execute terraform plan 

```sh
terrraform apply
```

- Validate newly created EC2 in AWS Console