kubectl apply -f dockerone-deployment.yaml

kubectl get deployments --show-labels=true

kubectl get deployments -l tier=frontend

kubectl describe deployments

kubectl scale deployment dockerone-deployment --replicas=5  

kubectl scale -f dockerone-deployment.yaml --replicas=3

kubectl delete deployment dockerone-deployment

kubectl delete -f dockerone-deployment.yaml

kubectl port-forward deployment/dockerone-deployment 8080

kubectl set image deployment/dockerone-deployment dockerone=dockerone:latest --record
