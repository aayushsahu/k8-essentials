#### create Minikube cluster
    minikube start --cpus 4 --memory 8192 --vm-driver hyperkit

#### install Prometheus-operator
###### add repos
    helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
    helm repo add stable https://charts.helm.sh/stable
    helm repo update

###### install chart
    helm install prometheus prometheus-community/kube-prometheus-stack

###### install chart with fixed version    
    helm install prometheus prometheus-community/kube-prometheus-stack --version "9.4.1"

###### Link to chart
[https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack]
