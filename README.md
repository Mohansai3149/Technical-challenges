
# Azure Terraform Three Tier architecture deployment pattern

This repository contains the terraform script. This script is set of deployment artifacts using terraform scripts which form a 3-tier architecture template to make it simple an orchestration engine (infrastructure as code). It allows you to deploy an example 3 tier architecture infrastructure environment (Level 0) and workload environments capable of hosting VM (Level 1). 
Pattern – Three Tier architecture deployment using terraform

### Step 1: Build and Deploy baseline state with network component 
 
#### Terraform script folder structure 
Below snapshot provide folder structure of terraform scripts.  
- Common-modules 
  * Resource Group
-	Level 0 
  * Azure resources
- Abstract resource layer
* VNET
* Subnet 
* NSG
* NSG association
* Route Table 
* Route table association
* VNET peering 
* Main Module (abstract layer)

### Steps to run terraform script 
#### Level 0 Pre-Requisites
1.	Ensure Level 0 terraform.tfvars is configured properly. 
2.	Login in interactive mode using az login 
3.	set the subscription using command  
```
az account set –subscription “subscription_name”
```
#### Level 0 Execution Steps
1.	Execute terraform script using below commands
* Terraform Init
*  Terraform Plan
* Terraform Apply

#### Terraform TFVAR input required

Update TFVAR file at Level 0 folder as per your requirements, You don’t required update any other terraform modules input parameters. Script will fetch from TFVAR and Terraform output state.  

```

### Step 2: Deploy VM and demo related items. 
#### Level 1 
 

#### Terraform script folder structure for step 2

#### Below snapshot provide folder structure of terraform scripts.  

-	Application Layer
-	NIC
-	Public IP
-	Virtual Machine

#### Level 1 Pre-Requisites
1.	Ensure Level 1 terraform.tfvars is configured properly. 
2.	Ensure All components of Level 0 are created
3.	set the subscription using command az account set –subscription “subscription_name”

#### Level 1 Execution Steps
1.	Execute terraform script using below commands
* Terraform Init
*  Terraform Plan
* Terraform Apply

#### Terraform TFVAR input required

Update TFVAR file at Level 1 folder as per your requirements, You don’t required update any other terraform modules input parameters. Script will fetch from TFVAR and Terraform output state.

# Thanks.......