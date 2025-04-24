📦 GitHub Actions CI/CD for Java App on AWS EKS
This project demonstrates how to build and deploy a Java Spring Boot application using GitHub Actions for a complete CI/CD pipeline. The application is deployed to a production-grade Kubernetes cluster on AWS EKS.

🚀 What This Project Covers
Continuous Integration (CI) on Pull Requests:

Checkout source code

Build the app using Maven

Run unit tests

Continuous Deployment (CD) on Merge to main:

Build and push Docker image to Amazon ECR

Update kubeconfig for EKS

Deploy the updated app to EKS using kubectl

🛠️ Tools Used

Tool	Purpose
Maven	Build the Java app
Docker + Amazon ECR	Build and store container images
EKS + kubectl	Deploy to Kubernetes
GitHub Actions	Automate CI/CD pipeline
GitHub Secrets	Store AWS credentials securely
🧱 CI/CD Workflow
mermaid
نسخ
تحرير
graph TD
A[Developer Push / PR] --> B[GitHub Actions]
B --> C[Build with Maven]
C --> D[Build Docker Image]
D --> E[Push to ECR]
E --> F[Deploy to EKS]
F --> G[App Live on Kubernetes!]
📁 Folder Structure
bash
نسخ
تحرير
.
├── .github/workflows/
│   ├── ci-pr.yml       # CI pipeline on PR
│   └── cd-deploy.yml   # CD pipeline on push to main
├── Dockerfile
├── pom.xml
├── src/
│   └── main/java/...
├── deployment.yaml
├── service.yaml
└── README.md
🔐 GitHub Secrets Required

Secret Key	Description
AWS_ACCESS_KEY_ID	IAM user access key
AWS_SECRET_ACCESS_KEY	IAM user secret key
AWS_REGION	AWS region (e.g., us-east-1)
ECR_REPO_URI	URI of the ECR repo
