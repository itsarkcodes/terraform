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

## Real Example:
Let's say you've deployed an AWS EC2 instance using Terraform, and you want to extract and display its public IP address as an output variable. Here's an example:
```tf
provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
}

output "public_ip" {
  value = aws_instance.example.public_ip
}
```
- Outputs:
> public_ip = 203.0.113.12
