az group create --name acidemo --location eastus

az container create --resource-group acidemo --name acidemo --image vijayshinva/dockerone --dns-name-label aci-demo --ports 80

az container show --resource-group acidemo --name acidemo --query "{FQDN:ipAddress.fqdn,ProvisioningState:provisioningState}" --out table

az container logs --resource-group acidemo --name acidemo

az container attach --resource-group acidemo --name acidemo

az container delete --resource-group acidemo --name acidemo

az container list --resource-group acidemo --output table

az group delete --name acidemo
