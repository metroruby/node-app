```bash
# by https://www.jenkins.io/doc/book/installing/kubernetes/#configure-helm
# 
kubectl create namespace jenkins
kubectl get namespaces

# 
helm repo add jenkinsci https://charts.jenkins.io
helm repo update
helm search repo jenkinsci

# 
kubectl apply -f jenkins-volume.yaml

# 
kubectl apply -f jenkins-sa.yaml

# 
chart=jenkinsci/jenkins
helm install jenkins -n jenkins -f jenkins-values.yaml $chart

# Get your 'admin' user password by running. admin, aCch4hbHQKNjF1H3m0tek5
jsonpath="{.data.jenkins-admin-password}"
secret=$(kubectl get secret -n jenkins jenkins -o jsonpath=$jsonpath)
echo $(echo $secret | base64 --decode)

```