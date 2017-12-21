# This template disables encryption on a running Windows VMs

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSudhakaraReddyEvuri%2Fazure-quickstart-templates%2Fsuredd-singlepass%2F201-decrypt-running-windows-vm-singlepass%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FSudhakaraReddyEvuri%2Fazure-quickstart-templates%2Fsuredd-singlepass%2F201-decrypt-running-windows-vm-singlepass%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

This template disables encryption on a running Windows VMs.

Singlepass AzureDiskEncryption for VMs is currently in preview. Consuming this feature requires enabling the preview feature on the subscription and setting up a key vault with 'EnabledForDiskEncryption' access policy using the Azure powershell cmdlets below 
1. Register-AzureRmProviderFeature -FeatureName "UnifiedDiskEncryptionForVMs" -ProviderNamespace "Microsoft.Compute"

