# Jenkins k8s deployment
Files to deploy Jenkins in Kubernetes

Cert-manager installation:
   ```bash
   helm repo add jetstack https://charts.jetstack.io
   helm repo update
   helm install   cert-manager jetstack/cert-manager   --namespace cert-manager   --create-namespace   --version v1.9.1   --set installCRDs=true
   ```
   
NGINX Ingress Controller installation:
  ```bash
  helm repo add nginx-stable https://helm.nginx.com/stable
  helm repo update
  helm install my-release nginx-stable/nginx-ingress
