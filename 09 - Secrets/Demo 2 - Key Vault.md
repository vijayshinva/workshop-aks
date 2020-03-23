az identity create -g <RESOURCE GROUP> -n <IDENTITY NAME>
az keyvault set-policy -n $KV_NAME --key-permissions get list --spn <YOUR AZURE MANAGED IDENTITY CLIENT ID>
az keyvault set-policy -n $KV_NAME --secret-permissions get list --spn <YOUR AZURE MANAGED IDENTITY CLIENT ID>
az keyvault set-policy -n $KV_NAME --certificate-permissions get list --spn <YOUR AZURE MANAGED IDENTITY CLIENT ID>

az vmss identity assign -g <RESOURCE GROUP> -n <K8S-AGENT-POOL-VMSS> --identities <IDENTITY NAME>

az vmss identity show -g <resource group>  -n <vmss scalset name> -o yaml


kubectl create -f https://raw.githubusercontent.com/Azure/kubernetes-keyvault-flexvol/master/deployment/kv-flexvol-installer.yaml

kubectl get pods -n kv


