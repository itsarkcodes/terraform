# Purpose of Terraform state
- The purpose of the state in Terraform is to track the current state of your infrastructure resources as defined in your configuration files.
- Terraform uses this state to understand what resources are already deployed, their configuration, and how they relate to each other

<details>
<summary>Example</summary>
Let's say you want to use Terraform to create an AWS EC2 instance. You define the instance's configuration, such as its size, AMI, and security groups, in a Terraform configuration file (usually with a **.tf** extension). When you run **terraform apply** to execute the configuration, Terraform reads the file, creates the instance in AWS, and records the current state of the instance (e.g., its unique identifier, IP address, etc.) in the state file.
</details>

## Use Case
1. **Tracking Changes:** The state file helps Terraform identify changes in your configuration over time. When you make updates to your configuration and apply those changes with terraform apply, Terraform compares the new configuration to the state to determine what needs to be created, modified, or deleted.

2. **Dependency Management:** Terraform uses the state to understand the relationships and dependencies between resources. For example, if you create a load balancer that targets instances, Terraform needs to know which instances are associated with that load balancer. The state file holds this information.

3. ** Collaboration:** If you're working with a team, sharing the state file allows everyone to have the same view of the infrastructure. It ensures that every team member is aware of the current state, which helps prevent conflicts and inconsistencies.

4. **Infrastructure History:** The state file acts as a record of your infrastructure's history. It helps you see what resources were created, modified, or deleted in each change, allowing you to understand past actions and track the evolution of your infrastructure.
