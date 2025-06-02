# Kubernetes Cluster with Minikube - DevOps Internship Task 5


## 📌 Overview
This repository documents my completion of **Task 5** from the DevOps Internship program, where I:
- Set up a local Kubernetes cluster using Minikube
- Deployed an Nginx web server application
- Created Kubernetes Services to expose the application
- Performed scaling operations
- Learned fundamental Kubernetes concepts

## 🛠️ Technologies Used
- **Minikube** - Local Kubernetes cluster
- **kubectl** - Kubernetes command-line tool
- **Docker** - Container runtime
- **YAML** - Configuration files
- **Nginx** - Web server for demonstration


## 🚀 Step-by-Step Implementation

### 1. Environment Setup
```bash
# Install kubectl and minikube
# Start the cluster
minikube start --driver=docker

# Verify cluster status
kubectl cluster-info
# Create deployment from YAML
kubectl apply -f deployment.yaml

# Verify deployment
kubectl get deployments
kubectl get pods

# Create service from YAML
kubectl apply -f service.yaml

# Get service URL
minikube service nginx-service --url

# Scale up to 4 replicas
kubectl scale deployment nginx-deployment --replicas=4

# Verify scaling
kubectl get pods

📷 Screenshots
1.Webpage
<img width="1440" alt="Screenshot 2025-06-02 at 10 40 15 AM" src="https://github.com/user-attachments/assets/6b1e22f9-3452-448d-a932-6e402a6a161a" />

2.complete termin
<img width="1440" alt="Screenshot 2025-06-02 at 10 35 34 AM" src="https://github.com/user-attachments/assets/2028feee-9886-4733-bd43-9d90f4e2d5cb" />
al

3.kubectl get pods
<img width="515" alt="Screenshot 2025-06-02 at 10 34 08 AM" src="https://github.com/user-attachments/assets/3e72bcd4-5937-48fe-b07b-5683dd4256d5" />

4.kubectl get services
<img width="574" alt="Screenshot 2025-06-02 at 10 35 22 AM" src="https://github.com/user-attachments/assets/ebeefad5-2fc7-4f44-a2bd-bbaae8c8979e" />

📚 Key Concepts Learned
Pods: Smallest deployable units in Kubernetes

Deployments: Manage pod replicas and updates

Services: Network endpoints for pods

Scaling: Horizontal pod autoscaling

kubectl: Essential Kubernetes CLI tool

