# This template enables encryption on a running Windows VMs

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fejarvi%2Fazure-quickstart-templates%2Fejarvi-singlepass%2F201-encrypt-running-linux-vm-singlepass%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fejarvi%2Fazure-quickstart-templates%2Fejarvi-singlepass%2F201-encrypt-running-linux-vm-singlepass%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

This template enables encryption on a running Linux VM that satisfies the prerequisites listed in the [Azure Disk Encryption FAQ](https://docs.microsoft.com/en-us/azure/security/azure-security-disk-encryption-faq).

Warning:  Single pass for Linux is still under development.  This template is for test purposes only.  It is unsupported and considered unsafe to use for production workloads as it references a test version of the extension that changes frequently.  

Singlepass AzureDiskEncryption for VMs is currently in preview. Consuming this feature requires enabling the preview feature on the subscription and setting up a key vault with 'EnabledForDiskEncryption' access policy using the Azure powershell cmdlets below 
1. Register-AzureRmProviderFeature -FeatureName "UnifiedDiskEncryptionForVMs" -ProviderNamespace "Microsoft.Compute"
2. Set-AzureRmKeyVaultAccessPolicy -ResourceGroupName <rgName> -VaultName <vaultName> -EnabledForDiskEncryption"
