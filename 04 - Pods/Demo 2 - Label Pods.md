kubectl get pods --show-labels

kubectl label pods poddemo owner=vijay

kubectl get pods --selector owner=vijay

kubectl get pods -l "env in (production, development)"

kubectl delete pods -l "env in (production, development)"
