# Terraform Kubernetes Deployment Pipeline

This Jenkins pipeline deploys a Kubernetes cluster on AWS using Terraform.

## Repositories

- **Terraform Code**: https://github.com/acwarya/terraform-k8s-aws.git
- **Pipeline Definition**: This repository

## Pipeline Features

-  Parameterized builds (plan/apply/destroy)
-  Manual approval gates
-  Clones Terraform code from separate repository
-  Supports multiple AWS regions
-  Customizable cluster names
-  Saves deployment outputs as artifacts

## Parameters

- **ACTION**: plan, apply, or destroy
- **CLUSTER_NAME**: Name for the Kubernetes cluster
- **AWS_REGION**: AWS region to deploy to
- **TERRAFORM_REPO**: Repository containing Terraform code
- **TERRAFORM_BRANCH**: Git branch to use

## Jenkins Setup

1. Create new Pipeline job
2. Configure:
   - Pipeline from SCM: Git
   - Repository: https://github.com/acwarya/jenkins-pipelines.git
   - Script Path: terraform-k8s/Jenkinsfile
3. Save and run

## Infrastructure Created

- 1 Master Node (t3.micro)
- 2 Worker Nodes (t3.micro)
- Custom VPC with subnet
- Internet Gateway
- Security Groups
- SSH Key Pair

## Cost

Estimated: ~$2-3/month (storage only, instances free tier)
