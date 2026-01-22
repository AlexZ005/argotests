# Commands to setup
Chart.yaml    https://github.com/argoproj/argo-helm/blob/main/charts/argo-cd/Chart.yaml
values.yaml   https://github.com/argoproj/argo-helm/blob/main/charts/argo-cd/values.yaml
helm install argo-cd argo/argo-cd --namespace argocd --create-namespace
helm repo add argo-cd https://argoproj.github.io/argo-helm
helm dep update charts/argo-cd/

>kubectl get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" -n argocd
