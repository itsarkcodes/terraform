# Meta-Argument
- Meta-arguments in Terraform provide additional functionality or behavior to resources and modules.
- They are not specific to a resource's primary functionality but rather modify how Terraform interacts with or manages those resources.
- These meta-arguments are typically defined within the block of a resource or module.

## Following are the Meta arguments

### 1. depends_on (Already seen)
- Eg:
```tf
resource "aws_instance" "example_instance" {
  # ... instance configuration ...

  depends_on = [aws_security_group.example_sg]
}
```
### 2. lifecycle (Already seen)
- Eg:
```tf
resource "aws_instance" "example_instance" {
  # ... instance configuration ...

  lifecycle {
    create_before_destroy = true
  }
}
```

### 3. count
- count is used for creating a specified number of resource instances
- It allows you to create a specified number of identical resource instances.
- You define a single block of the resource, and Terraform creates the specified number of instances based on the value set for ```count```.
- Eg:
```tf
resource "aws_instance" "example_instance" {
  ami   = "ami-12345678"
  instance_type = "t2.micro"
  count = 3
}
```
- Now the count in the above resource will create 3 resource with the same name. What if you want different name for each
- Well you can use list of variables
- Eg:  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/5f5c51f2-f9f5-4c88-b713-10209d115d6b) ![image](https://github.com/itsarkcodes/terraform/assets/87442305/e5065a38-c455-460a-99af-0f70265ed354)
- If you want to provide dynamic values to count according to variables, then do this
- Eg:  
![image](https://github.com/itsarkcodes/terraform/assets/87442305/d219745f-d4fb-42a0-ac3c-f2d2fb74101b)
- The length function provides length of a list 

## The Problem with the ```Count``` Meta-argument
- The count meta_argument works with a list type, meaning every element has an index position - as seen below - when you run the terraform state list command to list all resources in the terraform.tfstate file:
```
aws_instance.pets[0]
aws_instance.pets[1]
aws_instance.pets[2]
```
- If you remove any element that is not the last element in the list above, you would get unexpected infrastructure resource changes when you run terraform plan to see the execution plan.
- For example, if you remove the element at index 0 (i.e., pets.txt), the following happens:
  - The current element at index 1 (i.e., cows.txt) will now become the new element at index 0, i.e., cows.txt is now at index 0
  - The current element at index 2 (i.e., birds.txt) will now be the new element at index 1, i.e., birds.txt is now at index 1
  - There will be no element at index 3, and this index will be destroyed
- This is where the flexibility of the for_each meta-argument comes into play!!

### 4. For_each
- The ```for_each``` meta-argument is just another way to create multiple similar instances of an infrastructure resource in a more flexible way.
- It can be used in a resource, data, or module block.
- It works with a map or a set of strings, and it creates an instance for each item in a map or set.
- Let’s look at some examples of how for_each is used below.
Eg:
```tf
variable "filename" {
  type = set(string) # Changed to set of string
  default = [
    "/root/pets.txt",
    "/root/cows.txt",
    "/root/brids.txt",
  ]
}
```
- The resource block can also be written as:
```tf
resource "local_file" "pet" {
  for_each = var.filename
  filename = each.value
}
```
