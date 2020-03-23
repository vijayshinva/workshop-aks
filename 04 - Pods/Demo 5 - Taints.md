kubectl taint nodes aks-agentpool-39693419-vmss000000 project=testproject:NoSchedule
kubectl taint nodes aks-agentpool-39693419-vmss000001 project=testproject:NoSchedule
kubectl taint nodes aks-agentpool-39693419-vmss000002 project=testproject:NoSchedule
kubectl taint nodes virtual-node-aci-linux project=testproject:NoSchedule

kubectl get nodes -o json | jq '.items[].spec.taints'

kubectl taint nodes aks-agentpool-39693419-vmss000001 project=testproject:NoSchedule-