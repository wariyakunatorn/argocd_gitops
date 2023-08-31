# argocd_gitops

This repo will boostrap ArgoCD and install application under /apps folder

# Simple 2 steps
```
cd bootstrap
make
```

## Application list
|Name|URL|Password|
|---|---|---|
|ArgoCD|https://argocd.127-0-0-1.nip.io|kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d|
|Jenkins|http://jenkins.127-0-0-1.nip.io|kubectl get secret --namespace jenkins jenkins -o jsonpath="{.data.jenkins-admin-password}" | base64 --decode|
|Sonarqube|http://sonarqube.127-0-0-1.nip.io|username: admin password: admin|
