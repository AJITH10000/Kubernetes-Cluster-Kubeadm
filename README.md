# Kubernetes Hello App with Minikube

This project demonstrates deploying a simple app with Kubernetes using Minikube on Windows (Docker driver).

---

## Prerequisites

- Minikube installed (https://minikube.sigs.k8s.io/docs/start/)
- kubectl installed (https://kubernetes.io/docs/tasks/tools/)
- Docker installed and running on Windows

---

## Project Files

- `deployment.yaml` — Defines the deployment for the `hello` app (using nginx image)
- `service.yaml` — Defines the service to expose the deployment (NodePort type)

---

## Steps to Deploy

1. Start Minikube with Docker driver (if not already running):

   ```bash
   - minikube start --driver=docker

2. Apply the deployment:

   ```bash
   - kubectl apply -f deployment.yaml

3. Apply the service:

   ```bash
   - kubectl apply -f service.yaml

4. Check pods and service status:

    ```bash
    
   - kubectl get pods
   - kubectl get svc
 
 ## Accessing the Service

 1. Using Minikube service tunnel (recommended on Windows with Docker driver):

    ```bash

    - minikube service my-service

    - This will open your default browser to the service URL, typically something like:

        http://127.0.0.1:<random-port>

        Important : Keep the terminal window open while using the service, as the tunnel stops if you close it.
        

