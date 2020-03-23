az group create --name aksdemo --location eastus

az aks create --resource-group aksdemo --name akscluster --node-count 1 --enable-addons monitoring --generate-ssh-keys

az aks install-cli

az aks get-credentials --resource-group aksdemo --name akscluster

az aks browse --resource-group aksdemo --name akscluster

kubectl create clusterrolebinding kubernetes-dashboard --clusterrole=cluster-admin --serviceaccount=kube-system:kubernetes-dashboard

kubectl get nodes

kubectl config get-contexts

kubectl config use-context aksdemo

kubectl config set-context --current --namespace=workshop-aks

kubectl config view --minify | grep namespace:

