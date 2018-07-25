# Running docker swarm build with Terraform
Terrafom implementation of Docker swarm build process

## 1. Getting Started
These instructions will get you a copy of the docker swarm up and running on your azure cloud for development and testing purposes.

## 2. Prerequisites
minimum requerd software for running this script's:

   * [azure-cli 2.0](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)  
   * [terraform](https://www.terraform.io/downloads.html)
   * [git-scm](https://git-scm.com/downloads) 
   * [Azure portal account](https://portal.azure.com) 


## 3. Installing
**if you have all requared credentials for azure**: 

```
subscription_id = "<azure-subscription-id>"
tenant_id = "<tenant-returned-from-creating-a-service-principal>"
client_id = "<appId-returned-from-creating-a-service-principal>"
client_secret ="<password-returned-from-creating-a-service-principal>"
```
clone repository and modify file with credentials **terraform.tfvars** 

**if you need configuration from scrach**  
step by step guide:
  1. clone reposytory to you local machine or your enviroment
  2. [Set up Azure authentication](https://docs.microsoft.com/en-us/azure/terraform/terraform-create-vm-cluster-with-infrastructure)
  3. [Create an Azure service principal with Azure CLI 2.0](https://docs.microsoft.com/en-us/cli/azure/create-an-azure-service-principal-azure-cli?view=azure-cli-latest)
  4. [Configure Terraform environment variables](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/terraform-install-configure#configure-terraform-environment-variables)
  5. [Set up Terraform access to Azure](https://www.terraform.io/docs/providers/azurerm/authenticating_via_service_principal.html)
   

  **how to run**:
  go to dirrectory with cloned repository and run in command line:
  ```bash
  terraform init - Initialize a Terraform working directory
  terraform plan - Generate and show an execution plan
  terraform apply - Builds or changes infrastructure
  ```
  terraform apply can be parameterized with following format: 
```
 terraform apply -var 'location=eastus' -var 'vnet=np-eastus-10-166-99' -var 'vnet_addr=10.166.99'
```
to destroy infrastructure: 
```
terraform destroy - Destroy Terraform-managed infrastructure
```



## 4. Running the tests
still in progress...

## 5. Versioning
current version v0.1

## 6. References
   * [azure-cli 2.0](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)  
   * [terraform](https://www.terraform.io/downloads.html)
   * [git-scm](https://git-scm.com/downloads) 
   * [Azure portal account](https://portal.azure.com) 
