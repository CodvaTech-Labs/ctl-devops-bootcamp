
+++
title = "Configure Terraform - Windows"
weight = 7
chapter = false
pre = "<b> 1.3 </b>"
+++

To install Terraform on a Windows system, you can follow these steps:

1. Download the Terraform binary: 
   - Open a web browser and go to the Terraform website at https://www.terraform.io/downloads.html.
   - Scroll down to the "Terraform Core" section and locate the Windows version.
   - Click on the appropriate 64-bit or 32-bit download link depending on your system architecture. This will download a ZIP file containing the Terraform binary.

2. Extract the Terraform binary:
   - Locate the downloaded ZIP file, right-click on it, and select "Extract All" from the context menu.
   - Choose the destination folder where you want to extract the contents of the ZIP file.

3. Set up the PATH environment variable:
   - Open the Start menu and search for "Environment Variables".
   - Click on "Edit the system environment variables" to open the System Properties window.
   - In the System Properties window, click on the "Environment Variables" button.
   - In the "System variables" section, scroll down and find the "Path" variable. Select it and click on the "Edit" button.
   - In the "Edit Environment Variable" window, click on the "New" button and enter the path to the directory where you extracted the Terraform binary. For example, if you extracted it to "C:\terraform", enter that path.
   - Click "OK" to save the changes.

4. Verify the installation:
   - Open a new Command Prompt window by searching for "Command Prompt" in the Start menu.
   - Type `terraform --version` and press Enter.
   - If Terraform is correctly installed and the PATH environment variable is set up correctly, it will display the version of Terraform installed on your system.

That's it! You have successfully installed Terraform on your Windows system. You can now use Terraform commands to manage your infrastructure as code. Remember to consult the Terraform documentation for further guidance on using Terraform and setting up your configurations.