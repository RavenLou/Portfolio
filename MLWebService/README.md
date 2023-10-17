# Machine Learning Web Service

## Table of Contents
1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Procedure](#procedure)
    - [AWS EKS / Kubernetes Setup](#aws-eks--kubernetes-setup)
    - [Containerization](#containerization)
    - [Pushing the Image to a Repository](#pushing-the-image-to-a-repository)
    - [Resource Provisioning](#resource-provisioning)
    - [Create Job YAML files](#create-job-yaml-files)
    - [Exposing Image Classification](#exposing-image-classification)

<a name="overview"></a>
## 1. Overview
This project involves setting up a robust online service to provide image classification using neural networks. This service is exposed through a web server, managed via Kubernetes, and housed in Docker containers across a cluster of nodes.

<a name="requirements"></a>
## 2. Requirements
- AWS account (AWS Educate accounts are not compatible).
- Familiarity with one of the programming languages: Python 3, Javascript, Java, or Go.
- Tools: EKS, EC2, Kubernetes, Docker.
- Recommended to execute on an EC2 instance.

<a name="procedure"></a>
## 3. Procedure

<a name="aws-eks--kubernetes-setup"></a>
### 3.1 AWS EKS / Kubernetes Setup
- Prepare a host machine (recommended EC2 instance).
- Install `aws cli`, `kubectl`, and `eksctl`.
- Use the provided YAML file configuration for cluster setup.

<a name="containerization"></a>
### 3.2 Containerization
- Dockerize the classification script.
- Test the Docker container locally.

<a name="pushing-the-image-to-a-repository"></a>
### 3.3 Pushing the Image to a Repository
- Push the Docker image to AWS ECR or Dockerhub.

<a name="resource-provisioning"></a>
### 3.4 Resource Provisioning
- Create namespaces and allocate resources.
- Ensure proper resource management between free and premium services.

<a name="create-job-yaml-files"></a>
### 3.5 Create Job YAML Files
- Create YAML files for Kubernetes jobs.
- Specify image name, environment variables, and resource limits in the YAML files.

<a name="exposing-image-classification"></a>
### 3.6 Exposing Image Classification
- Implement a server that interacts with Kubernetes and handles incoming HTTP requests for image classification.
- Provide API endpoints for free and premium services and a configuration endpoint.

## References
- [EKS user guide](#)
- [Kubernetes documentation](#)
- [Video reference for EKS setup](#)
- [kubectl cheatsheet](#)
- [Creating a cluster with eksctl](#)
- [Docker resource](#)
- [Dockerhub reference](#)
- [AWS ECR documentation](#)
- [Configure Memory and CPU Quotas for a Namespace](#)

## Notes
- The server should handle requests and create Kubernetes jobs dynamically.
- Ensure all namespaces and resource quotas are configured correctly.
- Monitor your AWS resources to avoid charges.
- Debugging: Make sure to check the logs if you encounter issues with the Kubernetes jobs.

## Conclusion
This project encapsulates several aspects of modern cloud computing, from containerization to orchestration, and demands a solid understanding of various tools and principles. It's an excellent opportunity to experience real-world scenarios of providing machine learning as a service.
