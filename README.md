# 🚀 Kubernetes Multi-Node Cluster using Kind

---

## 📌 Project Overview

This project demonstrates how to create a **multi-node Kubernetes cluster** using Kind and deploy a containerized application using Kubernetes resources like Deployment, Service, and Ingress.

---

## ⚙️ Tools Used

* Kind (Kubernetes in Docker)
* Kubectl
* Docker
* Nginx

---

## 🧱 Cluster Architecture

* 1 Control Plane Node
* 2 Worker Nodes

---

## 🚀 Cluster Setup

### 1. Create Cluster

```bash
kind create cluster --config kind-config.yml
```

### 2. Verify Cluster

```bash
kubectl get nodes
```

---

## 🚀 Application Deployment

### Apply Kubernetes Resources

```bash
kubectl apply -f deployment.yml
kubectl apply -f service.yml
kubectl apply -f ingress.yml
```

### Verify Deployment

```bash
kubectl get pods
kubectl get svc
kubectl get ingress
```

---

## 🧱 Project Architecture

* Kind multi-node cluster
* Nginx deployment (2 replicas)
* NodePort service (Port: 30007)
* Ingress routing (nginx.local)

---

## 🌐 Application Access

### Option 1: Port Forward (Recommended)

```bash
kubectl port-forward --address 0.0.0.0 service/nginx-service 8080:80
```

Access in browser:

```
http://<EC2-IP>:8080
```

---

### Option 2: NodePort

```
http://<EC2-IP>:30007
```

---

## 📷 Output

### Cluster Nodes

<img width="802" height="451" alt="kind-cluster" src="https://github.com/user-attachments/assets/f4d9f65a-8247-4b17-a09d-ff423f8a5266" />

### Application Running

<img width="879" height="472" alt="image" src="https://github.com/user-attachments/assets/ec29a1a8-5086-4c7f-a998-a5938c3cedcf" />

---

## 🎯 Key Learnings

* Kubernetes cluster setup using Kind
* Deployment and scaling of applications
* Service exposure using NodePort
* Ingress configuration and routing
* Debugging networking issues in Kubernetes
* Git and GitHub workflow with SSH

---

## 🔮 Future Improvements

* Add CI/CD pipeline using GitHub Actions
* Deploy custom Docker application instead of Nginx
* Use Helm for package management
* Add monitoring (Prometheus + Grafana)

---

## 👨‍💻 Author

**Farman Ali**
DevOps & Cloud Enthusiast 🚀

---
