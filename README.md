# Create an Active Directory Forest backed up using Recovery Vault

This templates uses an [existing 
template](https://github.com/wkasdorp/forest-2-domains) to deploy a 
working Active Directory forest with two domains, a root named 
*fabrikam.com* and a child domain called *factory.fabrikam.com*. Each 
domain contains two DCs to keep things interesting. Then, it creates a 
Recovery Vault with a backup policy set to backup daily and to keep 
those backups for 60 days. This schedule is a sensible default for 
Domain Controllers. 

The goal of this template is to enable exercises with Azure-based Active 
Directory recovery. For this reason, the number of configurable options 
is kept to a minimum although it would be easy to extend the list if you 
wanted to.  

One-click deployment to Azure:

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwkasdorp%2Frecovery-vault-with-AD-forest%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

Warning: this template **creates four running VMs**. Make sure to deallocate them 
when you are done to avoid incurring costs. 

