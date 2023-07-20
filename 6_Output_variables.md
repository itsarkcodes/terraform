## Output Variables
- These variables can be used to store the value of an expression in terraform
Syntax:
```tf
output "<variable-name>" {
    value = "<variable_value>"
    <arguments>
}
```
Eg:
```tf
output "pet-name" {
  value = random_pet.my-pet.id
  description = "This is a description"
}
```  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/5b80d2f2-9730-42b5-b980-cd0dcb54253f)
 
## Terraform Output Command 
```terraform output``` Command print all the output variable defined in all the files in all the configuration directory  

![image](https://github.com/itsarkcodes/terraform/assets/87442305/09cee7fe-9027-404b-876f-9830ca221640)

![image](https://github.com/itsarkcodes/terraform/assets/87442305/1f4a68d3-33cc-4997-b3f7-eb11824aad99)

## Use Case
- Display details about provision resource on the screen
- To feed output variables to other IAC tools such as script or Ansible playbook
