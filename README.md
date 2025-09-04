# Install-ArgoCD
## Step 1: Install ArgoCD

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```

## Step 2: Login

```
argocd admin initial-password -n argocd
argocd login 192.168.1.139:30780 --username admin --password pGGkegD6GvHT4RQE
```

## Step 3: Add repo

```
argocd repo add https://github.com/TakawatP/demo.git   --username takawatp   --password [Token]
argocd app list
```
