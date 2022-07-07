## Terraform Provider for Azure (Resource Manager)

The AzureRM Terraform Provider allows managing resources within Azure Resource Manager.

When using version 3.0 of the AzureRM Provider we recommend using Terraform 1.x ([the latest version can be found here](https://www.terraform.io/downloads)). Whilst older versions of Terraform Core (0.12.x and later) remain compatible with v3.0 of the AzureRM Provider - support for versions prior to 1.0 will be removed in the next major release of the AzureRM Provider (v4.0).

* [Terraform Website](https://www.terraform.io)
* [AzureRM Provider Documentation](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs)

## Precondition
 * Login azure cli from your terminal
    ```sh
    $ az login
    ```
 * To use a specific Azure subscription, run az account set.
     ```sh
    $ az account set --subscription "<subscription_id_or_subscription_name>"
    ```
 * To create a service principal, run az ad sp create-for-rbac.
     ```sh
    $ az ad sp create-for-rbac --name <service_principal_name> --role Contributor --scopes /subscriptions/<subscription_id>
    ```
 * Get values from creating Service Princial, then export them
     ```sh
    $ export ARM_SUBSCRIPTION_ID="<azure_subscription_id>"
    $ export ARM_TENANT_ID="<azure_subscription_tenant_id>"
    $ export ARM_CLIENT_ID="<service_principal_appid>"
    $ export ARM_CLIENT_SECRET="<service_principal_password>"
    ```
    
## For Test1: Enable Kubernetes Role-Based Access Control - AKS
 * Go to Test1 folder 
 * Change values in file "terraform.tfvars"
   - `appId`
   - `password`
 * Run commands
    ```sh
    $ terraform init
    $ terraform plan
    $ terraform apply
    ```

## For Test5: Enable HTTP to HTTPS redirects for your Microsoft Azure App Service web applications
 * Go to Test5 folder 
 * Run commands
    ```sh
    $ terraform init
    $ terraform plan
    $ terraform apply
    ```
