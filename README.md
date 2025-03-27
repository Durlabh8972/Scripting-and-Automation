# PROG8830 – Practical Lab 8: Advanced Features in Terraform

*Course:* Infrastructure as Code (PROG8830)  
*College:* Conestoga College  
*Group Members:* Dhyeykumar Patel, Durlabh tilavat, Keerthana 
*Instructor:* Mike 
*Semester:* Winter 2025  

---

## Objective

The objective of this lab is to apply *advanced Terraform features* such as loops, functions, expressions, and dynamic infrastructure management in a real-world web application scenario. The infrastructure consists of compute instances, a load balancer, a database, and supporting resources.

## How to run
terraform init,
terraform plan,
terraform apply,

## Purpose and functionality
# Task 1: Using Terraform Loops
Purpose:
This task focuses on utilizing Terraform loops to efficiently provision multiple resources while demonstrating the differences between count and for_each.

Functionality:
count: Used to create multiple identical compute instances, simplifying infrastructure deployment when the number of resources is known in advance.

for_each: Enables provisioning of resources with unique attributes by iterating over a map or set, making it more flexible for dynamic configurations.

The configuration provisions multiple AWS EC2 instances using count and dynamically creates AWS security groups with varying ports and names using for_each.

# Task 2: Applying Functions in Terraform
Purpose:
To explore Terraform’s built-in functions to manipulate data, automate configurations, and enhance Infrastructure as Code (IaC) practices.

Functionality:
String functions: Convert text (e.g., upper(var.name)) to standardize resource names.

Numeric functions: Determine values dynamically, such as max(instance_count, 2), ensuring a minimum number of resources.

Collection functions: Manage lists/maps, e.g., concat(var.security_groups, ["default"]) to merge security groups.

Date/time functions: Automate time-based values, like tagging resources with deployment timestamps.

Networking functions: Use cidrsubnet() to efficiently allocate subnet addresses within a larger CIDR block.

# Task 3: Enhancing Terraform Configurations
Purpose:
To refactor and optimize Terraform code by incorporating advanced expressions and modularization, making configurations more scalable and maintainable.

Functionality:
Modularizes configurations using reusable modules, reducing code duplication.

Uses conditionals and expressions to dynamically adjust configurations based on input values.

Implements variable interpolation and data sources to enhance flexibility.

Improves readability and maintainability by structuring code efficiently.


