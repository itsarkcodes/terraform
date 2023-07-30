![image](https://github.com/itsarkcodes/terraform/assets/87442305/0edb86bf-0e42-4943-9802-9292031e0405)# More Commands

## 1. terraform validate
- Once we write are terraform config its not neccessary to execute ```terraform plan``` or ```terraform apply``` to check the syntax if its correct or not, we can use ```terraform validate```
- Allows you to validate the syntax and configuration of your Terraform files without actually applying them to your infrastructure
- If everything is correct we will see a successfull message  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/52c0ef69-faeb-4d10-baa8-2338a19af80b)

- If there is an error then we will see something like this  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/6fbb478d-dfc5-4951-9636-a531c50052d8)


## 2. terraform fmt (formet)
- ```terraform fmt``` scans the config files and automatically formats your Terraform configuration files to follow a standardized style.
- It helps ensure consistency and readability across your codebase by applying a consistent indentation, spacing, and line wrapping to your Terraform files.

Before:    
![image](https://github.com/itsarkcodes/terraform/assets/87442305/094e66a9-e432-4acc-bed9-4beccd220ee8)

After:  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/fcc66187-00d7-4e48-bd4c-7ae36603fa2d)

## 3. terraform show and terraform show -json
- ```terraform show``` used to inspect the current state of your infrastructure managed by Terraform.
- It provides a human-readable output that displays the resources and their attributes that have been created or modified by Terraform.    
![image](https://github.com/itsarkcodes/terraform/assets/87442305/175f4a08-bfc3-4391-ac87-a1305e60f3f5)

- ```terraform show -json``` command is an extension of the terraform show command. Instead of providing human-readable output, it generates the output in JSON format.  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/cd6668f9-b8ef-4ffc-ba62-33c0db43204b)
