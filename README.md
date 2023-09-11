# argocd_gitops

This repo will boostrap ArgoCD and install application under /apps folder

# Simple 2 steps
```
cd bootstrap
make
```

## Application list
1. ArgoCD  URL:  https://argocd.127-0-0-1.nip.io | Get Password ```kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d```
2. Jenkins  URL: http://jenkins.127-0-0-1.nip.io | Get Password ```kubectl get secret --namespace jenkins jenkins -o jsonpath="{.data.jenkins-admin-password}" | base64 --decode```
3. Sonarqube URL: http://sonarqube.127-0-0-1.nip.io ```username: admin password: admin```
