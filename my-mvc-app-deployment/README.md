# MyMvcApp Deployment

This repository contains the ARM template for deploying the MyMvcApp CRUD application to Azure.

## Project Structure

- `templates/mainTemplate.json`: The main ARM template that defines the resources to be deployed in Azure.
- `templates/parameters.json`: Contains parameters for the ARM template to customize deployment values.

## Prerequisites

- An Azure account with an active subscription.
- Azure CLI installed and configured on your local machine.
- Basic knowledge of Azure resources and ARM templates.

## Deployment Instructions

1. Clone this repository to your local machine.
2. Open a terminal and navigate to the project directory.
3. Log in to your Azure account using the Azure CLI:
   ```
   az login
   ```
4. Create a resource group (if you don't have one):
   ```
   az group create --name <your-resource-group-name> --location <your-location>
   ```
5. Deploy the ARM template using the following command:
   ```
   az deployment group create --resource-group <your-resource-group-name> --template-file templates/mainTemplate.json --parameters templates/parameters.json
   ```
6. Monitor the deployment process in the Azure portal.

## Notes

- Ensure that you customize the `parameters.json` file with your specific values before deployment.
- Refer to the Azure documentation for more details on ARM templates and resource management.