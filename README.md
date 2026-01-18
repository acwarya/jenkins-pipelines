# Jenkins Pipelines Repository

This repository contains Jenkins pipeline definitions for various infrastructure projects.

## Directory Structure

- **terraform-k8s/**: Kubernetes cluster deployment pipeline
  - Jenkinsfile: Main deployment pipeline
  - README.md: Documentation

## Repositories

- Terraform Code: https://github.com/acwarya/terraform-k8s-aws.git
- Jenkins Pipelines: https://github.com/acwarya/jenkins-pipelines.git

## Usage

In Jenkins, create a Pipeline job and point it to this repository:
- Repository URL: https://github.com/acwarya/jenkins-pipelines.git
- Script Path: terraform-k8s/Jenkinsfile
