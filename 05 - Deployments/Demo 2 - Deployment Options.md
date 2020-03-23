Rolling Update
===============

kubectl apply -f dockerone-deployment-red.yaml

kubectl rollout status deployment.v1.apps/dockerone-deployment

kubectl get rs

kubectl describe deployments

kubectl rollout history deployment.v1.apps/dockerone-deployment

kubectl rollout history deployment.v1.apps/dockerone-deployment --revision=2

kubectl rollout undo deployment.v1.apps/dockerone-deployment

kubectl rollout undo deployment.v1.apps/dockerone-deployment --to-revision=1

kubectl rollout status deployment.v1.apps/dockerone-deployment

TODO : How to edit rollout history

kubectl -it exec dockerone-deployment-7545d95bc7-4kh2b curl http://10.240.0.46:80

Recreate
=========

Blue-Green
==========

Canary
=======