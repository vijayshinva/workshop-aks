kubectl apply -f dockerone-config-map.yaml

kubectl get configmap

kubectl get configmap dockerone-settings -o yaml

kubectl create configmap dockerone-settings --from-env-file dockerone-config.txt

kubectl create configmap dockerone-settings --from-literal=log_level=verbose --from-literal=setting.1=setting.1.value

kubectl apply -f dockerone-deployment-config-env.yaml

kubectl apply -f dockerone-deployment-config-vol.yaml