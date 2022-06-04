
# Create CI/CD in Azure Pipeline using Helm Chart and Kubernetes

  

Here we're going to implement CI/CD (Auto Deployment) in Azure Pipeline using **Kubernetes** and **HelmChart**. HelmChart can manage your deployments automatically in your **K8s** cluster. So I've implemented a **Pipeline** template to create and deploy your project in Azure using **HelmChart**.

  
  

# Introduction
Here is YAML file as Azure Pipeline for our project in the current repo. You can define multiple pipelines if you have more than one project.

> deployment/pipeline/pipeline.yml

You can edit this YAML based on your project requirements. The features can include following items:

 - Define your **Environment variables**
 - Define your **Group variables**
 - Build and push your **Docker image**
 - Build and run your project **tests**
 - Install and pack the **HelmChart** as an **Artifact** to use in your deployment
 - Pack and push your sub-projects as **Nuget**

Also, you can **customize** the templates (add, remove or edit) which can satisfy your needs. Each template which is mentioned in the main Pipeline YAML file has its own parameters. These parameters can come from environment variables or define locally in YAML files. It's a good idea to define your frequently used parameters as group variables in Azure.

# Sample Code
I've created a sample code with this Azure Pipeline template for better comprehension. Please use your own parameters and user credentials in your environment.