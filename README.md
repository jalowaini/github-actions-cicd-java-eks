# GitHub Actions CI/CD for Java App on AWS EKS

This is a real DevOps project that shows how to build and deploy a Java Spring Boot app using GitHub Actions as a CI/CD tool.

The app is deployed to a Kubernetes Cluster (EKS) on AWS using a complete automated pipeline.

---

## What’s Covered

### CI – On Pull Request:
- Checkout code from GitHub
- Build app using Maven
- Run unit tests

### CD – On Push to `main`:
- Build Docker image
- Push image to Amazon ECR
- Update kubeconfig for EKS
- Deploy to EKS using `kubectl`

---

## Tools Used

| Tool               | Purpose                                |
|--------------------|----------------------------------------|
| Maven              | Build Java Spring Boot app             |
| Docker + Amazon ECR| Build and store Docker image           |
| EKS + kubectl      | Deploy to AWS-managed Kubernetes       |
| GitHub Actions     | Automate CI/CD workflow                |
| GitHub Secrets     | Store AWS credentials securely         |

---

## Required GitHub Secrets

| Secret Name             | Description                       |
|-------------------------|-----------------------------------|
| `AWS_ACCESS_KEY_ID`     | IAM access key                    |
| `AWS_SECRET_ACCESS_KEY` | IAM secret key                    |
| `AWS_REGION`            | AWS region (e.g. us-east-1)       |
| `ECR_REPO_URI`          | URI of your Amazon ECR repository |


---

## 👨‍💻 Author

Built with ❤️ by [@jalowaini](https://github.com/jalowaini)
