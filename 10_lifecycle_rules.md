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
3. 
