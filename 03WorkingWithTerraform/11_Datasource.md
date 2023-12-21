# Datasource
- data sources allow you to fetch information from external systems or resources that are not managed by Terraform itself.
- They enable you to import existing data into your Terraform configuration so that you can reference it within your infrastructure definitions or use it to make decisions during resource provisioning.

## Scenario
- Let's consider a case where you want to create an AWS EC2 instance and associate it with a security group. However, you don't want to define the security group within your Terraform configuration, as it already exists in your AWS account.
- **Solution:** You can use a data source to fetch the details of the existing security group and then reference that security group when creating your EC2 instance.
- 
