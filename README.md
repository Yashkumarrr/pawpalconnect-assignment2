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
```


In addition to manually deploying the application, this project can also be automated using Jenkins.

Jenkins can clone the repository, build the Docker image, push it to a container registry, and apply the Kubernetes manifests automatically.

This ensures repeatable, zero-downtime deployments without manual intervention.

The pipeline uses stages for checkout and deployment, and can also use environment variables or credentials for secure configuration.

This shows how the project supports both manual and automated deployment workflows, demonstrating real-world DevOps practices.

##images

<img width="1920" height="875" alt="Screenshot 2026-01-06 144742" src="https://github.com/user-attachments/assets/f30167ac-ae46-4695-b3c4-7db3204af648" />


<img width="1079" height="631" alt="Screenshot 2026-01-06 150418" src="https://github.com/user-attachments/assets/5ba8babb-5563-4318-bbd8-02f82c8f8c4d" />
