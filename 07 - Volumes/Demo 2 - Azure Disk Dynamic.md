kubectl get sc

kubectl apply -f pv-azure-managed-disk.yaml

kubectl apply -f dockerone-deployment-azure-managed-disk.yaml

kubectl rollout status deployment.v1.apps/dockerone-deployment

kubectl get pvc azure-managed-disk

az disk list --query "[].id | [?contains(@,'pvc-e4fdc488-6ad5-11ea-8421-3eab8fcf37f1')]" -o tsv