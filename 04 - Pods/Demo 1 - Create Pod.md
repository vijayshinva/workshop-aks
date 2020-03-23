kubectl run nginx --image=nginx --restart=Never

kubectl apply -f dockerone-pod.yaml

kubectl delete -f pod.yaml

kubectl replace -f pod.yaml

kubectl port-forward poddemo 8080:80

kubectl exec poddemo -it sh

kubectl exec poddemo -it curl bing.com

kubectl top pod dockerone-deployment-7d6b8d8b7f-bpfhk --containers