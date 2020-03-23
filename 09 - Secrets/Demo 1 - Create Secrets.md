kubectl create secret generic dockerone-secrets --from-literal=.connection-string=VmlqYXlzaGludmEgS2FybnVyZQ==

kubectl create secret tls dockerone-secrets --cert=path_to_cert --key=path_to_key

kubectl create configmap dockerone-secrets --from-file=.connection-string=dockerone-secrets.txt

kubectl apply -f dockerone-secrets.yaml

kubectl get secrets

kubectl get configmap dockerone-settings -o yaml





kubectl apply -f dockerone-deployment-config-env.yaml

kubectl apply -f dockerone-deployment-config-vol.yaml