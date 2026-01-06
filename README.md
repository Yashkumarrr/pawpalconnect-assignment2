# pawpalconnect-assignment2


This project demonstrates deploying a simple Node.js application to Kubernetes using Docker and Minikube.

## What is included
- Dockerfile to containerize the application
- Kubernetes manifests for:
  - Deployment
  - Service
  - ConfigMap
  - Secret
- Readiness and liveness probes
- Rolling updates for zero downtime

## Prerequisites
- Docker
- kubectl
- Minikube

## Run locally
```bash
docker build -t assess .
docker run -p 3000:3000 assess
docker tag assess yashkashyapp/assess:assessment
docker push yashkashyapp/assess:assessment
kubectl apply -f service.yml
kubectl apply -f configmap.yml
kubectl apply -f deployment.yml
kubectl apply -f secret.yml


##images

<img width="1920" height="875" alt="Screenshot 2026-01-06 144742" src="https://github.com/user-attachments/assets/f30167ac-ae46-4695-b3c4-7db3204af648" />


<img width="1079" height="631" alt="Screenshot 2026-01-06 150418" src="https://github.com/user-attachments/assets/5ba8babb-5563-4318-bbd8-02f82c8f8c4d" />
