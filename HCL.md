# HashiCorp Configuration Language

## HCL Syntax:
- The HCL file consist of blocks and arguments

![image](https://github.com/itsarkcodes/terraform/assets/87442305/c0e4c48d-deec-44f4-8941-70f76dc4f805)

- A block is defined between curly braces {} and arguments in key value formet representing the configuration data
- A block in terraform contains information about set of resources within that platform that we want to create

![image](https://github.com/itsarkcodes/terraform/assets/87442305/14f87ee5-661f-4a8a-a22f-919f083bd815)

Eg: Resource file created for provisioning for AWS instance
![image](https://github.com/itsarkcodes/terraform/assets/87442305/945a3349-e2e7-4fa3-acfb-f53ac1ee8929)

## Terraform Workflow
Terraform Workflow consist of 4 different steps:
1. Write the configuration file
2. Run `terraform init` command
- This checks the configuration file and initialize the working dir containing the .tf file
- It will download the plugins
4. Review the execution plan using `terraform plan` command
- This command will show the actions that will be carried out by Terraform to create the resource

![image](https://github.com/itsarkcodes/terraform/assets/87442305/b5aeb55d-4f2c-4ffc-aa61-82ea8d319a01)

- The `+` symbol implies that the resource will be created
- This step will not create the infrastructure resource yet. This step is only for reviewing the actions that will be performed
5. Once ready, Apply the changes using `terraform apply` command
- This cmd will display the execution plan once again and ask user to confirm and then it will create

![image](https://github.com/itsarkcodes/terraform/assets/87442305/f2fffee2-e3e6-4fcd-a42b-0d6784f00248)

5. We can use `terraform show` cmd to see what resources we have created

![image](https://github.com/itsarkcodes/terraform/assets/87442305/e967e115-9a0b-4453-a279-2200b40e727c)



