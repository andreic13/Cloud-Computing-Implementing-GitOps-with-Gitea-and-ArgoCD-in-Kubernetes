# Cloud-Computing-Implementing-GitOps-with-Gitea-and-ArgoCD-in-Kubernetes

## Objective
The goal of this project is to learn GitOps principles by setting up a continuous deployment pipeline using Gitea and ArgoCD within a Kubernetes cluster. Aquired knowledge:

- Install and configure Gitea as a self-hosted Git service.
- Install and configure ArgoCD to manage application deployments from Gitea repositories.
- Deploy a web application using ArgoCD.
- Implement a liveness probe for the Nginx application to ensure its health and availability.
- Package their builds for easy redeployment.

### Task 1: Create a Kubernetes Cluster

Initialize a Kubernetes cluster using Kind.
Configure kubectl to use the new cluster.
Verify the cluster status and ensure nodes are ready.

### Task 2: Install Gitea
Create a namespace for Gitea.
Add the Gitea Helm repository.
Install Gitea using Helm.
Expose Gitea service to access the web interface. Hint: proxy to your browser.

Complete the initial Gitea setup:
Register a new user.
Create a repository named nginx-deployment.

### Task 3: Install ArgoCD

Create a namespace for ArgoCD.
Install ArgoCD.
Expose the ArgoCD server. Hint: proxy to your browser.

Log in to ArgoCD.
Connect the Gitea repository to ArgoCD.

### Task 4: Deploy Nginx with ArgoCD

For this task, you are going to deploy your own cloud-courses page.

Create a Kubernetes manifest for an Nginx Reverse Proxy deployment and service to host your own cloud-courses page in your Gitea repository.
Push the manifest to the Gitea repository.
Create an ArgoCD application that points to the repository and deploys the manifest.
Apply the ArgoCD application manifest.
Verify that the Nginx deployment and service are running.

### Task 5: Add Liveness Probe to Nginx

Modify the deployment manifest to include a liveness probe.
Push the updated manifest to Gitea.
Confirm that ArgoCD syncs the changes and redeploys the application.
Verify that the liveness probe is configured correctly.

### Task 6: Package the Nginx with Helm

Create a Helm chart that deploys the previously configured Nginx deployment and service.
Publish the package on your Gitea repository. Hint: use the package registry.
Verify that your Helm chart deploys the previously configured Nginx deployment and service.
