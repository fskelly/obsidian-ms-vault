Resources 
| where type == "microsoft.compute/virtualmachines"
| where tostring(properties.storageProfile.osDisk.osType) == "Windows"
| where properties['licenseType'] == "" // ##Empty seems to imply NO AHUB - value in here - seems to imply AHUB

Resources
| where type contains "microsoft.compute/disks"
| project Os=properties.osType,
DiskSku=sku.name,
DiskSizeGB=properties.diskSizeGB,
id = managedBy
| join (Resources | where type == "microsoft.compute/virtualmachines") on id
| where DiskSizeGB != 128 or DiskSizeGB !=64 
##add other sizes

