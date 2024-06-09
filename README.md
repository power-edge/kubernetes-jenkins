# Kubernetes Manifests for Jenkins Deployment

Refer https://devopscube.com/setup-jenkins-on-kubernetes-cluster/ for step by step process to use these manifests.

## Deployment
1. `kubectl apply -f namespace.yaml`
2. `kubectl apply -f serviceAccount.yaml`
3. `kubectl create -f volume.yaml`
  > Important Note: Replace worker-node01 with any one of your cluster worker nodes hostname.<br>
  > You can get the worker node hostname using the kubectl: `kubectl get nodes`
4. `kubectl apply -f deployment.yaml`

* Check deployment status

`kubectl get deployments -n devops-tools`

* Get deployment details

`kubectl  describe deployments --namespace=devops-tools`