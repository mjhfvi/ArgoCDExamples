## build jenkins with arcgcd
# argocd config file for jenkins
argocd-jenkins.yaml

# jenkins value file
values-jenkins.yaml

# run command
argocd app create jenkins -f argocd-jenkins.yaml --values values-jenkins.yaml


## Remove
argocd app delete jenkins


## argocd app create jenkins -f argocd-jenkins.yaml --values-literal-file values-jenkins.yaml ## LOCAL FILE
## argocd app create jenkins -f argocd-jenkins.yaml --values values-jenkins.yaml ## FILE IN REPO
## argocd app delete jenkins

## argocd login localhost:8080