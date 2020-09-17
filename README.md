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
   ### Pre-requisites
   1. AWS Account
   2. DockerHub Account
   3. GitHub Account
   4. GitHub Personal Access Token: [How to create access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) 
   5. Kubernetes Cluster  (See below for sample kubeconfig.yaml) 
   5. Git repository with DockerFile and helm chart
        ![GitHub Repo](github-repo.png)
      
  ### OpenShift Deployment 
   The following configuration files are required. You can upload configuration files to an S3 bucket or place it at the root directory of repository.
   1. kubeconfig.yaml
   2. database-secret.yaml (optional)
   
   Sample OCP configuration files: <https://github.com/mcmpdemo/home/tree/master/mcmp-demo-config-bucket/OCP>
   
   
  ### EKS Deployment
  The following configuration files are required. You can upload configuration files to an S3 bucket or place it at the root directory of repository.
   
   1. kubeconfig.yaml
   2. database-secret.yaml (optional)
   3. credentials
   4. config
   
   Sample EKS configuration files: <https://github.com/mcmpdemo/home/tree/master/mcmp-demo-config-bucket/EKS>
   
  ### Provisioning Pipeline
   **From MCMP console **
   1. Login to MCMP
   2. Select **Enterprise Marketplace** => **Catalog**
   3. Select **AWS CI/CD Pipeline** => **Configure**
   
   **From AWS console**
   <a href="https://console.aws.amazon.com/cloudformation/home?#/stacks/new?&templateURL=https://mcmp-demo-config-bucket.s3.us-east-2.amazonaws.com/mcmp-pipeline-cloudformation-github.yaml" rel="nofollow"><img src="../images/cloudformation-launch-stack.png" alt="deploy to aws" style="max-width:100%;"></a>
   
   

