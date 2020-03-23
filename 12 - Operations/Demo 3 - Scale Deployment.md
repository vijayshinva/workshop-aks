git clone https://github.com/kubernetes-incubator/metrics-server.git
kubectl create -f metrics-server/deploy/1.8+/


kubectl autoscale deployment azure-vote-front --cpu-percent=50 --min=3 --max=10

kubectl apply -f dockerone-deployment-autoscale.yaml

kubectl get hpa