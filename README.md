<!-- TOC --><a name="table-of-contents"></a>
# Table of Contents


- [Web server environment using terraform](#web-server-environment-using-terraform)
   * [Challenge Overview](#challenge-overview)
   * [Assumptions](#assumptions)
   * [Technical Requirements](#technical-requirements)
      + [Network](#network)
      + [Compute](#compute)
      + [Supporting Infrastructure](#supporting-infrastructure)

<!-- TOC end -->

<!-- TOC --><a name="web-server-environment-using-terraform"></a>
# Web app environment
This challenge provides a hands-on experience in setting up a basic Azure environment using Terraform, a popular Infrastructure as Code (IaC) tool.

By working through this challenge, students will gain practical skills in using Terraform to automate and manage cloud infrastructure, which is a crucial aspect of modern DevOps practices.

This challenge is ideal for those looking to deepen their understanding of Terraform and its application in real-world scenarios, making it a valuable addition to any DevOps curriculum.


## What You Will Create

In this challenge, students will create a fully functional web server environment on Azure using Terraform. The environment will include:

- A virtual network with subnets for network segmentation.
- An Azure App Service to host the web application.
- Azure Function Apps for background tasks and API endpoints.
- A storage account for application data and logs.
- An Azure Key Vault for secure storage of secrets and certificates.
- Azure API Management for managing and securing APIs.

By the end of this challenge, students will have a comprehensive understanding of how to use Terraform to deploy and manage cloud infrastructure on Azure.


<!-- TOC --><a name="challenge-overview"></a>
## Challenge Overview

Create a proof-of-concept Azure environment using Terraform. The environment will host a basic web server with proper network segmentation and security controls. Use open source terraform modules such as
 
- [Microsoft Repositories](https://github.com/orgs/Azure/repositories?q=terraform-azurerm)  

 The use of Terraform modules is required.


<!-- TOC --><a name="assumptions"></a>
## Assumptions
- The user has access to an Azure subscription with sufficient permissions to create the required resources.
- Terraform and Azure CLI are installed and configured on the user's machine.


<!-- TOC --><a name="technical-requirements"></a>

## Technical Requirements

### Network
- **Virtual Network**: Create a virtual network with at least two subnets to separate the web server and database tiers.

### Compute
- **App Services**: Deploy an Azure App Service to host the web application.
- **Function Apps**: Create two Azure Function Apps for handling background tasks and API endpoints.

### Storage
- **Storage Account**: Provision a storage account for storing application data, logs, and other necessary files.

### Security
- **Key Vault**: Set up an Azure Key Vault to securely store secrets, keys, and certificates.

### API Management
- **API Management**: Implement Azure API Management to manage and secure the APIs exposed by the web application and function apps.

