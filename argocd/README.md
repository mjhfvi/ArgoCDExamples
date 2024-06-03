### build argocd applications with arcgcd
## argocd config file for argocd-apps, values-argocd-apps.yaml
# run command
argocd app create argocd-apps -f argocd-apps.yaml

## argocd config file for argocd-image-updater, argocd-image-updater.yaml
# run command
argocd app create argocd-image-updater -f argocd-image-updater.yaml

## argocd config file for argo-events, argo-events.yaml
# run command
argocd app create argo-events -f argo-events.yaml

## argocd config file for argo-rollouts, argo-rollouts.yaml
# run command
argocd app create argo-rollouts -f argo-rollouts.yaml

## argocd config file for argo-workflows, argo-workflows.yaml
# run command
argocd app create argo-workflows -f argo-workflows.yaml