# Install-ArgoCD
Step 1: Install ArgoCD

'''
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
'''
