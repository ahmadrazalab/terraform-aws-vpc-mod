
# Custom VPC Module 🌐

Easily create a custom VPC in the **ap-south-1** region, complete with public and private subnets, route tables, and security groups. Perfect for your AWS infrastructure!

- 🌍 **Custom VPC**  
- 🌐 **Public & Private Subnets**  
- 🚪 **Route Tables**  
- 🌐 **NAT Gateway & Static IP**  
- 🔒 **Security Groups**  
- 🔄 **Internet Gateway**  

## What Does It Do?

This module helps you quickly create a secure and scalable VPC setup:

- **Custom VPC**: A dedicated virtual network with full control over your IP address range.  
- **Subnets**: Create both public and private subnets for separating your workloads.  
- **Route Tables**: Automatically configure route tables for routing traffic between subnets.  
- **NAT Gateway**: Provides outbound internet access for resources in private subnets.  
- **Security Groups**: Define inbound and outbound traffic rules for your instances.  
- **Internet Gateway**: Allows instances in public subnets to access the internet.  

## Getting Started 🚀

### Requirements  
1. **AWS CLI** installed and configured.  
2. **Terraform 1.x+** installed.  
3. **IAM Permissions** for creating VPCs, subnets, NAT Gateways, and route tables.  

### Example Use

```hcl
module "vpc_setup" {
  source        = "./custom-vpc-module"
  region        = "ap-south-1"
  vpc_cidr      = "10.0.0.0/16"
  public_subnet_cidr = "10.0.1.0/24"
  private_subnet_cidr = "10.0.2.0/24"
  enable_nat_gateway = true
  enable_internet_gateway = true
  sg_name        = "my-app-sg"
}

```

### Outputs  
- ✅ VPC ID  
- ✅ Public Subnet IDs  
- ✅ Private Subnet IDs  
- ✅ NAT Gateway ID  
- ✅ Internet Gateway ID  
- ✅ Security Group ID  

## Why Use This Module?

- **Simple**: Create a full-featured VPC setup with minimal effort.  
- **Scalable**: Easily extendable with more subnets, route tables, and security groups.  
- **Secure**: Private and public subnets with robust security groups and internet access control.  

---

For more, visit my blog: [docs.ahmadraza.in](https://docs.ahmadraza.in)  
