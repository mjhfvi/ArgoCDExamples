## build traefik with arcgcd
# add service and ingress
kubectl -f traefik-service.yaml apply

# argocd config file for traefik
argocd-traefik.yaml

# jenkins value file
values-traefik.yaml

# run command
argocd app create traefik -f argocd-traefik.yaml --values values-traefik.yaml



kubectl port-forward $(kubectl -n traefik get pods --selector "app.kubernetes.io/name=traefik" --output=name) 9000:9000


## Remove
argocd app delete traefik


argocd app create traefik -f argocd-traefik.yaml
argocd app create traefik -f argocd-traefik.yaml --values values-traefik.yaml ## FILE IN REPO
argocd app create traefik -f argocd-traefik.yaml --values-literal-file values-traefik.yaml ## LOCAL FILE
argocd app delete traefik
