# ARM

## Install Az Module in Powershell
Install-Module -Name Az -Repository PSGallery -Force

## Connect to Azure
Connect-AzAccount

## Create rg-test resource group
New-AzResourceGroup `
  -Name rg-test `
  -Location "Central US"

# Run the template
New-AzResourceGroupDeployment `
  -Name azuredeploy `
  -ResourceGroupName rg-test `
  -TemplateFile azuredeploy.json
