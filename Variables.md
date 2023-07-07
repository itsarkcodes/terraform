# Input Variables
- To assign variables we have to create new configuration file called `variable.tf`
- `variable.tf` consist of blocks and arguments
- To create variable we need to use the keyword `variable` followed by the variable name
- Within the block we can provide the default value which is an optional parameter
  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/81ddd4a0-1e5b-471d-a6ce-fc772032f36c)

- To use the variable in our main.tf file we can replace the argument values with the variable names prefixed with `var`
  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/8ead8856-8aba-4e0f-b20d-0df710e6f7c4)

- Now we can perform the normal execution by `terraform plan` and `terraform apply`
- If you have changed the variable values than you have to use `terraform apply` to recreate the resources

### EG: How configuration file looks like when creating aws instance with terraform

![image](https://github.com/itsarkcodes/terraform/assets/87442305/e6d591d4-cd00-4c5f-b87a-d9298f4ee7d3)
