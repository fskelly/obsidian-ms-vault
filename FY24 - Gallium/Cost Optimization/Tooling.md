Resources 

| where type == "microsoft.compute/virtualmachines"
| where tostring(properties.storageProfile.osDisk.osType) == "Windows"
| where properties['licenseType'] == "" //##Empty seems to imply NO AHUB - value in here - seems to imply AHUB

VHD sizes 
- Obscure sizes

Stopped vm versus stopped (dealloacted)

AHUB benfits ARG query
- then run script on these resources