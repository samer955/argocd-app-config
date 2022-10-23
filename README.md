# argocd-app-config
How to deploy and run the app as a network service with minikube/kubernetes Manifest and using ArgoCD to Continuous Delivery.

See application.yaml for the ArgoCD configuration.


If using Windows or WSL2: minikube start --ports=127.0.0.1:port:port (where 'port' is the service port where you want to expose th application)

App is exposed to localhost:port or 127.0.0.1:port
