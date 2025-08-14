# 🚀 Task 5: Build a Kubernetes Cluster Locally with Minikube

## 📌 Objective
Deploy and manage applications in Kubernetes using **Minikube**, **kubectl**, and **Docker**.

---

## 🛠 Tools Used
- 🖥 **Minikube** – Local Kubernetes cluster
- 📦 **kubectl** – Kubernetes command-line tool
- 🐳 **Docker** – Container runtime

---

## 📂 Deliverables
- Kubernetes YAML files: `deployment.yaml`, `service.yaml`  
- Screenshot of pods/services: `kube.png`  

---

## 📜 Steps to Complete the Task

### **1-Command Setup & Deployment**
```bash
# Start Minikube
minikube start && \

# Apply Deployment and Service
kubectl apply -f deployment.yaml && \
kubectl apply -f service.yaml && \

# Verify Pods
kubectl get pods && \

# Scale Deployment
kubectl scale deployment <deployment-name> --replicas=3 && \

# Check Pod Details and Logs
kubectl get pods && \
kubectl describe pod $(kubectl get pods -o jsonpath='{.items[0].metadata.name}') && \
kubectl logs $(kubectl get pods -o jsonpath='{.items[0].metadata.name}')
