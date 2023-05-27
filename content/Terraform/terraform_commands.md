+++
title = "Terraform Commands"
weight = 10
chapter = false
pre = "<b> 1.6 </b>"
+++

- The command line interface to Terraform is via the terraform command, which accepts a variety of subcommands such as terraform init or terraform plan.

### terraform help : 
- Terraform has a built-in help system that can be accessed from the command line for commands that you are not familiar with, or want to learn more about. You can get specific help for any specific command, use the -help option with the relevant subcommand.

```sh
nilesh@Nileshs-MacBook-Air import-demo % terraform -help
Usage: terraform [global options] <subcommand> [args]
```

The available commands for execution are listed below.
The primary workflow commands are given first, followed by
less common or more advanced commands.

```sh
Main commands:
  init          Prepare your working directory for other commands
  validate      Check whether the configuration is valid
  plan          Show changes required by the current configuration
  apply         Create or update infrastructure
  destroy       Destroy previously-created infrastructure
All other commands:
  console       Try Terraform expressions at an interactive command prompt
  fmt           Reformat your configuration in the standard style
  force-unlock  Release a stuck lock on the current workspace
  get           Install or upgrade remote Terraform modules
  graph         Generate a Graphviz graph of the steps in an operation
  import        Associate existing infrastructure with a Terraform resource
  login         Obtain and save credentials for a remote host
  logout        Remove locally-stored credentials for a remote host
  output        Show output values from your root module
  providers     Show the providers required for this configuration
  refresh       Update the state to match remote systems
  show          Show the current state or a saved plan
  state         Advanced state management
  taint         Mark a resource instance as not fully functional
  test          Experimental support for module integration testing
  untaint       Remove the 'tainted' state from a resource instance
  version       Show the current Terraform version
  workspace     Workspace management
Global options (use these before the subcommand, if any):
  -chdir=DIR    Switch to a different working directory before executing the
                given subcommand.
  -help         Show this help output, or the help for a specified subcommand.
  -version      An alias for the "version" subcommand.

```

### terraform init
- The terraform init command is used to initialise a working directory containing terraform configuration files. This is the first command that should be run after writing a new Terraform configuration or cloning an existing one from version control. It is safe to run this command multiple times.

```sh
terraform init 
```

### terraform plan
- The terraform plan command is used to create an execution plan.

It will not modify things in infrastructure.Terraform performs a refresh, unless explicitly disabled, and then determines what actions are necessary to achieve the desired state specified in the configuration files.

This command is a convenient way to check whether the execution plan for a set of changes matches your expectations without making any changes to real resources or to the state.

```sh
terraform plan Creates an execution plan (dry run)
terraform plan -out=path save generated plan output as a file
terraform plan -destroy Outputs a destroy plan

```

```sh
terraform plan


```

### terraform apply
- The terraform apply command is used to apply the changes required to reach the desired state of the configuration. Terraform apply will also write data to the terraform.tfstate file.

Once the application is completed, resources are immediately available.

terraform apply’ : Executes changes to the actual environment
terraform apply –auto-approve : Apply changes without being prompted to enter ”yes”
terraform apply -refresh=true : Update the state for each resource prior to planning and applying
terraform apply -input=false : Ask for input for variables if not directly set
terraform apply -var ‘foo=bar’ : Set a variable in the Terraform configuration, can be used multiple times
terraform apply -var-file=foo : Specify a file that contains key/value pairs for variable values
terraform apply -target : Only apply/deploy changes to the targeted resource

```sh
terraform apply

```

### terraform refresh
- The terraform refresh command reads the current settings from all managed remote objects and updates the Terraform state to match. This does not modify infrastructure but does modify the state file.

```sh
terraform refresh

```

### terraform validate
- The terraform validate command validates the configuration files in a directory.Validate runs checks that verify whether a configuration is syntactically valid and thus primarily useful for general verification of reusable modules, including the correctness of attribute names and value types.

```sh
nilesh@Nileshs-MacBook-Air ec2-demo % terraform validate
Success! The configuration is valid.
```sh

### terraform graph
- The terraform graph command is used to generate a visual representation of either a configuration or execution plan. The output is in the DOT format, which can be used by GraphViz to generate charts.

```sh
terraform graph | dot -Tsvg > graph.svg
```

### terraform fmt
- The terraform fmt command is used to rewrite Terraform configuration files to a canonical format and style. This command applies a subset of the Terraform language style conventions, along with other minor adjustments for readability.

-recursive — Also process files in subdirectories. By default, only the given directory (or current directory) is processed.

```sh
nilesh@Nileshs-MacBook-Air ec2-demo % terraform fmt
```

### terraform output
- The terraform output command is used to extract the value of an output variable from the state file.

```sh
terraform output
```

### terraform show
- The terraform show command is used to provide human-readable output from a state or plan file.This can be used to inspect a plan to ensure that the planned operations are expected, or to inspect the current state as Terraform sees it.

```sh
terraform show
```

### terraform taint
- The terraform taint command informs Terraform that a particular object has become degraded or damaged. Terraform represents this by marking the object as “tainted” in the Terraform state, and Terraform will propose to replace it in the next plan you create.

```sh
terraform taint
```

### untaint
- If Terraform currently considers a particular object as tainted but you’ve determined that it’s actually functioning correctly and need not be replaced, you can use terraform untaint to remove the taint marker from that object.

This command will not modify any real remote objects, but will modify the state in order to remove the tainted status.

```sh
terraform untaint
```

### terraform replace
For Terraform v0.15.2 and later, terraform recommend using the -replace option with terraform apply to force Terraform to replace an object even though there are no configuration changes that would require it.

The change will be reflected in the Terraform plan, letting you understand how it will affect your infrastructure before you take any externally-visible action.

- When you use terraform taint, other users could create a new plan against your tainted object before you can review the effects terraform taint aws_instance.web (mark resource as tainted and then we need to terraform apply)

### terraform version
This command will print terraform version

```sh
terraform — version
```

### terraform workspace
The terraform workspace command is used to manage workspaces.

```sh
The terraform workspace new command is used to create a new workspace.
The terraform workspace list command is used to list all existing workspaces.
The terraform workspace show command is used to output the current workspace.
The terraform workspace select command is used to choose a different workspace to use for further operations.
The terraform workspace delete command is used to delete a workspace.

```sh
terraform workspace list
terraform workspace new dev
terraform workspace list
terraform workspace select dev
terraform workspace delete dev
terraform workspace select default
terraform workspace delete dev    
terraform workspace show
```

###  terraform import
The terraform import command is used to import existing resources into Terraform. Import will find the existing resource from ID and import it into your Terraform state at the given ADDRESS. ADDRESS must be a valid resource address. Because any resource address is valid, the import command can import resources into modules as well as directly into the root of your state.

- Use Case : Suppose there is one ec2 instance which is already provisioned in AWS and now you want to to import that ec2 instance in terraform code.

- Manually Created EC2 Instance in AWS

```sh
Example :

# Sample_Terraform_Code
resource “aws_instance” “import_demo” {
}
nilesh@Nileshs-MacBook-Air import-demo % terraform init
nilesh@Nileshs-MacBook-Air import-demo % terraform import 

### terraform destroy
- The terraform destroy command is used to destroy the terraform-managed infrastructure. Terraform destroy command is not the only command through which infrastructure can be destroyed.You can remove the resource block from the configuration and run terraform apply this way you can destroy the infrastructure.

```sh
terraform destroy –auto-approve : Destroy/cleanup without being prompted to enter ”yes”
terraform destroy -target : Only destroy the targeted resource and its dependencies
```

```sh
terraform destory
```

- References :
https://www.terraform.io/cli/commands