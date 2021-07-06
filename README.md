#  Argo CD with Helm 
### Setup Argo CD on a Kubernetes cluster. We’ll install it with Helm

* Creating a Helm chart

  - `helm repo add argo-cd https://argoproj.github.io/ argo-helm`

  - `helm dep update charts/argo-cd/`


*  Installing the Argo CD Helm chart
   - `helm install argo-cd charts/argo-cd/`


* Accessing the Web UI
   - `kubectl port-forward svc/argo-cd-argocd-server 8080:443`
   - The password is auto-generated and defaults to the pod name of the Argo CD server pod. We can get it with"
    `kubectl get pods -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2`


    




