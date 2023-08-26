# 🌱 Terraform Lifecycle:

### When you use Terraform to manage your infrastructure as code, it goes through several phases in its lifecycle:
### Initialization > Planning > Apply > Destroy(If needed)

## Lifecycle rules:
1. Create Before Destroy:
- Sometimes, when you need to change a resource, Terraform might need to destroy the existing one and then create a new one to apply the changes.
- ```create_before_destroy = true``` for a resource, Terraform will create the new resource before destroying the old one.
- This can help in scenarios where you want to ensure there's no downtime during updates.  
Eg:
```tf
resource "local_file" "pet" {
  filename = "/roots/pet.txt"
  content = "Hello pet"
  file_permission = "0700"

  lifecycle {
    create_before_destroy = true
  }
}
```
![image](https://github.com/itsarkcodes/terraform/assets/87442305/75892820-69bd-4e08-909c-5b37c0803f2a)

2. Prevent Destroy:
-  Imagine you have a critical resource that you never want to accidentally destroy, like a database holding important data.
-  You can use the ```prevent_destroy``` argument to prevent Terraform from destroying that resource.
-  This adds an extra layer of safety, ensuring that such resources can't be deleted by mistake.
Eg: 
```tf
resource "local_file" "pet" {
  filename = "/roots/pet.txt"
  content = "Hello pet"
  file_permission = "0700"

  lifecycle {
    prevent_destroy = true
  }
}
```
