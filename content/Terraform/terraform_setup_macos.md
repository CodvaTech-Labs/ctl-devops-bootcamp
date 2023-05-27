+++
title = "Configure Terraform - Mac OS"
weight = 8
chapter = false
pre = "<b> 1.4 </b>"
+++

To install Terraform on macOS using Homebrew, you can follow these steps:

1. Open the Terminal application. You can find it in the "Utilities" folder within the "Applications" folder.

2. Install Homebrew (if not already installed): In the Terminal, paste the following command and press Enter:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
This command will install Homebrew, a package manager for macOS.

3. Install Terraform: In the Terminal, run the following command to install Terraform using Homebrew:
```sh
brew install terraform
```
This command will download and install the latest version of Terraform from the Homebrew repository.

4. Verify the installation: After the installation is complete, you can verify if Terraform is installed correctly by running the following command in the Terminal:
```sh
terraform --version
```
If the installation was successful, it will display the version of Terraform installed on your system.

That's it! You have successfully installed Terraform on your macOS system using Homebrew. You can now use Terraform commands to manage your infrastructure as code. Make sure to consult the Terraform documentation for further guidance on using Terraform and setting up your configurations.