az aks scale --resource-group aksdemo --name akscluster --node-count 5




az aks nodepool update --enable-cluster-autoscaler

az aks update --resource-group aksdemo --name akscluster --update-cluster-autoscaler  --min-count 1 --max-count 5