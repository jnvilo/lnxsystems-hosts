curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
bash get_helm.sh 
helm repo add awx-operator https://ansible.github.io/awx-operator/
helm repo update
helm install -n awx --create-namespace my-awx-operator awx-operator/awx-operator

