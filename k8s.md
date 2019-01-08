# Kubernetes

## [Helm](https://helm.sh/)

### Up

1. Install Helm
2. Init it: `helm init` (you need to wait few seconds for tiller to be ready)

```bash
helm install -f values.local.yaml --name test --namespace=default .
```

### Down

```bash
helm del --purge test
```

### Upgrade

```bash
helm upgrade -f values.local.yaml test .
```

### Install Helm on GKE

```bash
gcloud container clusters get-credentials cluster-name --zone europe-west1-b
helm init
kubectl create serviceaccount --namespace kube-system tiller
kubectl create clusterrolebinding tiller-cluster-rule --clusterrole=cluster-admin --serviceaccount=kube-system:tiller
kubectl patch deploy --namespace kube-system tiller-deploy -p '{"spec":{"template":{"spec":{"serviceAccount":"tiller"}}}}'
helm init --service-account tiller --upgrade
```

### Deploy nginx controller

```bash
kubectl create clusterrolebinding cluster-admin-binding --clusterrole cluster-admin --user $(gcloud config get-value account)
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/mandatory.yaml
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/provider/cloud-generic.yaml
```

### Create basic auth

```bash
htpasswd -c auth username
kubectl create secret generic basic-auth --from-file=auth
```

## Local Kubernetes Dashboard

```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v1.10.1/src/deploy/recommended/kubernetes-dashboard.yaml
kubectl proxy
```