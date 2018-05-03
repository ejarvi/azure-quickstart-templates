# This template disables encryption of a Linux VM with no AAD

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fejarvi%2Fazure-quickstart-templates%2Fejarvi-singlepass%2F201-encrypt-running-windows-vm-singlepass%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fejarvi%2Fazure-quickstart-templates%2Fejarvi-singlepass%2F201-encrypt-running-windows-vm-singlepass%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

This template disables encryption of data disks on a running Linux VM with no AAD if only data disks were encrypted.   If the OS disk was also encrypted, this scenario is not supported and is expected to fail. 

Singlepass AzureDiskEncryption for VMs is currently in preview. Consuming this feature requires enabling the preview feature on the subscription and setting up a key vault with 'EnabledForDiskEncryption' access policy using the Azure powershell cmdlets below 
1. Register-AzureRmProviderFeature -FeatureName "UnifiedDiskEncryptionForVMs" -ProviderNamespace "Microsoft.Compute"
2. Set-AzureRmKeyVaultAccessPolicy -ResourceGroupName <rgName> -VaultName <vaultName> -EnabledForDiskEncryption"
