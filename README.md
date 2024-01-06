# Jenkins_on_K8s_Pods

### Prerequisites
- Install Docker
- Install Minikube

### Run the following commands
```
Start the Docker Desktop (Windows) or run "service start docker"(Linux)
kubectl create -n jenkins 
minikube start
kubectl apply -f . 
kubectl get all -A
kubectl port-forward svc/jenkins -n jenkins 3000:8080 --address 0.0.0.0
access Jenkins on "http://localhost:3000"

```
### Get Jenkins Password
<div align="center"> <a href=""><img src="https://drive.google.com/file/d/1YQZr_RLfU-WsuMbeBrUEQ94plXdtyJib/view?usp=sharing" alt='image' width='800'/></a> </div>

       

