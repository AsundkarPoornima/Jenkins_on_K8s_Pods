# Jenkins_on_K8s_Pods

Start the Docker Desktop (Windows) or run "service start docker"(Linux)
kubectl create -n jenkins 
minikube start
kubectl apply -f . 
kubectl get all -A
kubectl port-forward svc/jenkins -n jenkins 3000:8080 --address 0.0.0.0

       

