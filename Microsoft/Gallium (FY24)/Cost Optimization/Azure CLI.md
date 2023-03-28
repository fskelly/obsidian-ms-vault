You can also use [Install WSL | Microsoft Learn](https://learn.microsoft.com/en-us/windows/wsl/install) with Azure Cli
[How to install the Azure CLI | Microsoft Learn](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)

az extension add --name resource-graph

resources 
| where type == 'microsoft.compute/virtualmachines'
| where tostring(properties.storageProfile.osDisk.osType) == 'Windows'
| where properties['licenseType'] == ''

az graph query -q "resources 
| where type == 'microsoft.compute/virtualmachines'
| where tostring(properties.storageProfile.osDisk.osType) == 'Windows'
| where properties['licenseType'] == ''" -o table