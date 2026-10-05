# Terraform Docker Infrastructure as Code

## Project Overview

This project demonstrates Infrastructure as Code (IaC) using Terraform to provision a local Docker container.

Terraform was used with the Docker provider to:

- Pull the Nginx Docker image
- Create an Nginx Docker container
- Map container port 80 to host port 8081
- Verify the running container
- Inspect Terraform state
- Destroy the infrastructure

## Tools Used

- Terraform v1.12.2
- Docker v29.8.1
- Nginx
- Git
- GitHub

## Project Structure

```text
terraform-docker-task/
├── main.tf
├── README.md
├── .gitignore
└── screenshots/
Terraform Workflow
1. Initialize Terraform
terraform init

Initialized Terraform and installed the Docker provider.

2. Review Infrastructure Plan
terraform plan

Terraform planned:

2 to add, 0 to change, 0 to destroy

Resources:

docker_image.nginx
docker_container.nginx
3. Provision Infrastructure
terraform apply

Terraform successfully created the Nginx image and container.

4. Verify Docker Container
docker ps

The container was running with:

Container: terraform-nginx
Host Port: 8081
Container Port: 80
5. Test Nginx
curl http://localhost:8081

The Nginx welcome page was successfully returned.

6. Check Terraform State
terraform state list

Terraform tracked:

docker_container.nginx
docker_image.nginx
7. Destroy Infrastructure
terraform destroy

Terraform successfully destroyed both resources.

2 resources destroyed
What I Learned
Infrastructure as Code concepts
Terraform providers
Terraform resources
Terraform state
terraform init
terraform plan
terraform apply
terraform destroy
Resource dependencies
Docker container provisioning using Terraform
Outcome

Successfully provisioned and destroyed a local Nginx Docker container using Terraform.

The task demonstrates the basic IaC workflow:

terraform init
        ↓
terraform plan
        ↓
terraform apply
        ↓
verify infrastructure
        ↓
terraform state
        ↓
terraform destroy
