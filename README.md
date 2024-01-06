# Jenkins_on_K8s_Pods

### Prerequisites
- Install Docker
- Install Minikube
- Clone the Jenkins_on_Minikube_Pods Repo in local

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

Setup the new Password and Install Docker,Kubernetes Plugins
<div align="center"> <a href=""><img src="https://github.com/AsundkarPoornima/Jenkins_on_Minikube_Pods/blob/main/images/jenkins_pass.jpg" alt='image' width='800'/></a> </div>

### Add Cloud

Go to Dashboard>Manage Jenkins>Clouds
Click on create New Cloud and details given below and click on Test Connection
<div align="center"> <a href=""><img src="https://github.com/AsundkarPoornima/Jenkins_on_Minikube_Pods/blob/main/images/SS_Jenkins_Cloud.jpg" alt='image' width='800'/></a> </div>

Below that add Pod label given as below and Save.
<div align="center"> <a href=""><img src="https://github.com/AsundkarPoornima/Jenkins_on_Minikube_Pods/blob/main/images/pod%20label.jpg" alt='image' width='800'/></a> </div>

Navigate to POD Template at left side and click on New POD Template. Add the POD template with the details, as shown in the image below.
<div align="center"> <a href=""><img src="https://github.com/AsundkarPoornima/Jenkins_on_Minikube_Pods/blob/main/images/pod%20template.jpg" alt='image' width='800'/></a> </div>

Add the container template with the details, as shown in the image below ans Save.
<div align="center"> <a href=""><img src="https://github.com/AsundkarPoornima/Jenkins_on_Minikube_Pods/blob/main/images/container_template.jpg" alt='image' width='800'/></a> </div>

### Test 

Go to Jenkins home –> New Item and create a freestyle project.
<div align="center"> <a href=""><img src="https://github.com/AsundkarPoornima/Jenkins_on_Minikube_Pods/blob/main/images/create_freestyle.jpg" alt='image' width='800'/></a> </div>

Add a "Execute shell" with an command to validate the job as shown below.
```
echo "testing"
```
<div align="center"> <a href=""><img src="https://github.com/AsundkarPoornima/Jenkins_on_Minikube_Pods/blob/main/images/test_pipeline.jpg" alt='image' width='800'/></a> </div>



       

