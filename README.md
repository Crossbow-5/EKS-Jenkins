CI/CD Pipeline for Kubernetes (EKS) App Deployment

Automated the deployment of an application (voting app) onto a Kubernetes cluster hosted on **Amazon EKS**.

The pipeline performs tasks like:
- Deploying Kubernetes resources (Deployments, Services, Ingress)
- Setting up Ingress routing for multiple apps
- Destroying resources conditionally
- Verifying Kubernetes access and cluster health

1.Deploy Voting App
Deploys a sample voting app using:

1.votingapp.yml

2. Deploy Ingress for Vote & Result UI
Sets up ingress rules:

2.ingress.yml
3.ingress-nk.yml

3. Deploy FastAPI Microservice with Ingress
Deploys a FastAPI service and configures routing:

4.fastapi-deployment.yml
5.fast-Ingress.yml

Deploy FastAPI Microservice with Ingress
Deploys a FastAPI service and configures routing:

4.fastapi-deployment.yml
5.fast-Ingress.yml

Deployment Validation
Lists all current K8s resources for visibility:
kubectl get pods,deployment,svc,ing

Requirements:
Jenkins agent with:
Terraform, Packer, Ansible, Docker
AWS CLI installed and configured, 
kubectl configured
Jenkins credentials set up to access AWS
Amazon EKS cluster: my-eks-cluster in us-east-1
