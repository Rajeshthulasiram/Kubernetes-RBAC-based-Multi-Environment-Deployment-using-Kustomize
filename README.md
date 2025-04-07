# Kubernetes-RBAC-based-Multi-Environment-Deployment-using-Kustomize

🧱 Step-by-Step Breakdown
🔹 Step 1: Create the folder structure
Run the following commands:
mkdir -p k8s-rbac-deploy-kustomize/{base,overlays/dev,overlays/prod}
cd k8s-rbac-deploy-kustomize

✅ Project Name: Kubernetes-RBAC-based-Multi-Environment-Deployment-using-Kustomize
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

✅ Step
Check resources created:
kubectl get all -n dev
kubectl get sa,role,rolebinding -n dev

kubectl get all -n prod
kubectl get sa,role,rolebinding -n prod

