# Argocd test application deployment
How to deploy and run the app as a network service with kubernetes Manifest, using ArgoCD to Continuous Delivery.

See application.yaml for the ArgoCD configuration.

Port Forwarding to access ArgoCD API without exposing the service:

``kubectl port-forward svc/argocd-server -n argocd 8080:443``

The API server can then be accessed using https://localhost:8080

user and password see: https://argo-cd.readthedocs.io/en/stable/getting_started/

## Deployment

`kubectl apply -f application.yaml` to deploy the application.

`kubectl get ingress -A` to get the ingress address and port.

`curl address:port` or in the browser to access the app.

The status of the application can be monitored in the ArgoCD API --> https://localhost:8080

If using WSL2: minikube start --ports=127.0.0.1:port:port (where 'port' is the service port where you want to expose th application)

App is exposed to localhost:port
