## build kubernetes-dashboard with arcgcd
# add service and ingress
kubectl -f kubernetes-dashboard-service.yaml apply

# argocd config file for kubernetes-dashboard
argocd-kubernetes-dashboard.yaml

# jenkins value file
values-kubernetes-dashboard.yaml

# run command
argocd app create kubernetes-dashboard -f argocd-kubernetes-dashboard.yaml --values values-kubernetes-dashboard.yaml


## Remove
argocd app delete kubernetes-dashboard


## argocd app create kubernetes-dashboard -f argocd-kubernetes-dashboard.yaml
## argocd app create kubernetes-dashboard -f argocd-kubernetes-dashboard.yaml --values values-kubernetes-dashboard.yaml ## FILE IN REPO
## argocd app create kubernetes-dashboard -f argocd-kubernetes-dashboard.yaml --values-literal-file values-kubernetes-dashboard.yaml ## LOCAL FILE
## argocd app delete kubernetes-dashboard

# get login Bearer Token
kubectl -n kubernetes-dashboard create token dashboard-user
