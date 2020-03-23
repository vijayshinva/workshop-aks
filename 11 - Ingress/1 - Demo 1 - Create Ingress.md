helm repo add stable https://kubernetes-charts.storage.googleapis.com/

helm install nginx-ingress stable/nginx-ingress --set controller.replicaCount=2 --set controller.nodeSelector."beta\.kubernetes\.io/os"=linux --set defaultBackend.nodeSelector."beta\.kubernetes\.io/os"=linux

kubectl get service -l app=nginx-ingress 

kubectl apply -f dockerone-ingress.yaml