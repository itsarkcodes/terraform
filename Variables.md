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


## Different Arguments in variables
1. default: Specify default values
2. type: Type of variable (Optional)
3. description: Description about variable (Optional)

![image](https://github.com/itsarkcodes/terraform/assets/87442305/be20a41b-8fd5-45f9-a5a8-554a3e3b2d1e)

## Basic Variable Types:
string, number, bool, any

**If no variable type provided than it will be set to type `any` by default**

## Additional Variable Types:
list, map, object, tuple

## 1. List
- A list is a numbered collection of values
Syntax:

![image](https://github.com/itsarkcodes/terraform/assets/87442305/1a1414e2-38e4-4b9f-bfe4-ff15515e6732)

- Each element in the list can be referenced by the number or index within that list
- Index of the List always begain with 0

![image](https://github.com/itsarkcodes/terraform/assets/87442305/3ef35633-d913-44d3-a7d2-95448e001bbc)

- These variables can be accessed like this

![image](https://github.com/itsarkcodes/terraform/assets/87442305/e436103a-b4a8-465a-b315-4c2157d8b531)


