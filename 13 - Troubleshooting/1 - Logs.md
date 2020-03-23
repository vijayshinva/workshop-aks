kubectl describe service dockerone-service-lb

kubectl describe deployment dockerone-deployment

kubectl describe pod dockerone-deployment-59c68f46-j9qm7

kubectl exec -ti dockerone-deployment-59c68f46-j9qm7 sh

kubectl logs dockerone-deployment-59c68f46-j9qm7

kubectl logs dockerone-deployment-59c68f46-j9qm7 dockerone

kubectl logs dockerone-deployment-59c68f46-j9qm7 -p

kubectl logs dockerone-deployment-59c68f46-j9qm7 -f

