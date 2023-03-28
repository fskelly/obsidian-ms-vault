[Install the Azure Az PowerShell module | Microsoft Learn](https://learn.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-9.5.0)

Install-Module -Name Az.ResourceGraph

$query = "
Resources 
| where type == 'microsoft.compute/virtualmachines'
| where tostring(properties.storageProfile.osDisk.osType) == 'Windows'
| where properties['licenseType'] == ''
"

$results = Search-AzGraph -Query $query