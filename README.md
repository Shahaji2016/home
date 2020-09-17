# AWS CI/CD Pipeline with Kubernetes, Helm and MCMP Integration

---
## Pipeline Overview 
![CFN AWS Pipeline](aws-overview.png)

---
## Deployment to Multiple Clusters
![CFN AWS Pipeline](aws-multiple-clusters.png)

---
## MCMP Integration - Build Instrumentation
![CFN AWS Pipeline](aws-pipeline-mcmp-integration.png)

## Instructions : Provisioning AWS CI/CD Pipeline
   The pipeline is designed to integrate with source code repository that contains a docker based application/microservice and deployed using helm chart.
   It is currently tested with GitHub repository and deployment to OpenShift/AWS-EKS Kubernetes clusters.
   # Pre-requisites
   
     1. AWS Account
     2. DockerHub Account
     3. GitHub Account
     4. GitHub Personal Access Token: [How to create access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) 
     5. Git repository with DockerFile and helm chart
        ![GitHub Repo](GitHub Repo.png)
      
## OpenShift Deployment 
   <https://github.com/mcmpdemo/home/tree/master/mcmp-demo-config-bucket/OCP>
   1. kubeconfig.yaml
   2. database-secret.yaml (optional)
   
## EKS Deployment
   <https://github.com/mcmpdemo/home/tree/master/mcmp-demo-config-bucket/EKS>
   1. kubeconfig.yaml
   2. database-secret.yaml (optional)
   3. credentials
   4. config

