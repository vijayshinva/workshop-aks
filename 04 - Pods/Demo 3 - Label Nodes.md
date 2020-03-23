kubectl get nodes --show-labels --output=wide

kubectl label nodes aks-agentpool-39693419-vmss000000 customlabel=vijay

kubectl apply -f dockerone-pod-nodeselector.yaml

kubectl label node aks-agentpool-39693419-vmss000000 customlabel-