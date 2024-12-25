# cicd-Argocd-manifests-repo

# Kubernetes Cluster

Ensure you have a running Kubernetes cluster (Minikube, EKS, GKE, AKS, etc.).
Ensure kubectl is configured to communicate with the cluster.

# Install ArgoCD on Kubernetes

# Create the argocd Namespace

kubectl create namespace argocd

# Apply the ArgoCD Installation YAML

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml


# Check if ArgoCD pods are running:

kubectl get pods -n argocd

# Create a Git repository for your Kubernetes manifests.

# Add your repository to ArgoCD via CLI or UI:

argocd repo add https://github.com/yourusername/your-repo.git --username <your-username> --password <your-password>

# Create an ArgoCD Application

kubectl apply -f Argocd-application/
