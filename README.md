# Kubernetes Python Microservice 

A simple Python Flask microservice deployed using Kubernetes on Docker Desktop.

##  Tech Stack

- Python 3.10 + Flask
- Docker
- Kubernetes (via Docker Desktop)
- `kubectl`

##  Project Structure

k8s-python-microservice/
├── app/
│ ├── app.py # Flask web app
│ └── requirements.txt # Python dependencies
├── Dockerfile # Image definition
├── k8s/
│ ├── deployment.yaml # Kubernetes Deployment
│ └── service.yaml # Kubernetes Service (NodePort)
└── README.md

##  How to Run It

### 1. Build Docker Image

docker build -t flask-k8s:latest .

### 2. Enable Kubernetes
Ensure Kubernetes is enabled in Docker Desktop.

### 3. Deploy to Kubernetes

kubectl apply -f k8s/

### 4. Access the Service
Check NodePort and open your browser:

kubectl get service flask-service
Default: http://localhost:30007

## To Tear Down

kubectl delete -f k8s/

## TODO / Enhancements

Add Prometheus + Grafana for monitoring

Use Helm for packaging

Add Ingress with TLS (optional)

Author
ViorelH – Kubernetes microservice demo for DevOps portfolio
