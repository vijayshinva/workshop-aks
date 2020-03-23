kubectl expose deployment dockerone-deployment --type=NodePort --name=dockerone-nodeport-service

kubectl apply -f dockerone-service-loadbalancer.yaml

kubectl -it exec dockerone-deployment-7545d95bc7-4kh2b curl curl dockerone-service-lb

kubectl port-forward service/dockerone-deployment 8080