# ☸️ Kubernetes Microservices Deployment

This project sets up multiple microservices using Kubernetes YAML manifests. Each service is containerized and deployed in a modular, scalable fashion.

---

## 📦 Microservices List

| 🔢 Service     | 📝 Description                     |
|---------------|-------------------------------------|
| 🛒 `cart`       | Manages user shopping carts         |
| 📚 `catalogue`  | Handles product listing/catalog      |
| 🐞 `debug`      | Internal debugging/testing pod       |
| 🌐 `frontend`   | Web interface for end users          |
| 🧑‍💻 `user`      | Manages user accounts and login      |
| 💳 `payment`    | Payment gateway microservice         |
| 🚚 `shipping`   | Shipping address & logistics         |

---

## 🗄️ Database Services

| 🧩 Database   | 🗃️ Type          | 📌 Used By           |
|--------------|------------------|----------------------|
| 🐘 `mongodb`  | NoSQL Document DB | User, Catalogue      |
| 🐬 `mysql`    | SQL Relational DB | Shipping             |
| 🐰 `rabbitmq` | Message Broker    | Payment, Shipping    |
| 🧠 `redis`    | In-memory Store   | Cart, Session Store  |

---

## 🏗️ Infrastructure Pods

| 🧰 Component   | 🔍 Role                         |
|---------------|---------------------------------|
| ⚙️ `instance` | Core backend pod/infrastructure |
| 🧪 `debug`    | Troubleshooting inside cluster  |

---

## 🚀 Deployment Steps

1. 🗂️ Apply Namespace  
2. ⚙️ Create ConfigMaps and Secrets  
3. 🛠️ Deploy Databases  
4. 🧩 Deploy Microservices  
5. 🌍 Expose Services (ClusterIP/NodePort/LoadBalancer)  

---

## ✅ Useful Commands

```bash
kubectl get all -n <namespace>            # List all resources
kubectl logs <pod-name> -n <namespace>    # View logs
kubectl describe svc <svc-name> -n <ns>   # Inspect service
kubectl apply -f <file>.yaml              # Deploy a resource

🛠️ Tools Used
    Kubernetes 🧬
    Docker 🐳
    YAML ⚙️
    VS Code 🖥️