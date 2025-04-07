# Kubernetes-RBAC-based-Multi-Environment-Deployment-using-Kustomize

✅ Project Name: k8s-rbac-deploy-kustomize
🗂 Folder Structure:
k8s-rbac-deploy-kustomize/
├── base/
│   ├── deployment.yaml
│   ├── namespace.yaml
│   ├── role.yaml
│   ├── rolebinding.yaml
│   ├── serviceaccount.yaml
│   └── kustomization.yaml
├── overlays/
│   ├── dev/
│   │   ├── patch-deployment.yaml
│   │   ├── namespace-patch.yaml
│   │   └── kustomization.yaml
│   └── prod/
│       ├── patch-deployment.yaml
│       ├── namespace-patch.yaml
│       └── kustomization.yaml


🚀 How to Deploy:
# Deploy to dev
kubectl apply -k overlays/dev/

# Deploy to prod
kubectl apply -k overlays/prod/
