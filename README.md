# GitOps-Project

# ---------Conneting AKS---------
<p align="left">az login</p>
<p align="left">az account show</p>
<p align="left">az configure --defaults group=openenv-55njs</p>
<p align="left">az aks get-credential --name aks-gitops-project</p>
<p align="left">az aks install-cli</p>
<p align="left">az aks get-credentials -g $RG --name aks-gitops-project</p>

<p align="left">kubectl get nodes</p>
<p align="left">kubectl create namespace argocd</p>
<p align="left">kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml</p>
<p align="left">kubectl port-forward svc/argocd-server -n argocd 8080:443   #Acceder localhost</p>
<p align="left">kubectl patch svc argocd-server -n argocd --type='json' -p '[{"op": "replace", "path": "/spec/type", "value": "LoadBalancer"}]'   #Acceder por IP publica</p>
<p align="left">kubectl get secret argocd-initial-admin-secret -n argocd -o yaml      #Entrega la contraseña encriptada</p>

