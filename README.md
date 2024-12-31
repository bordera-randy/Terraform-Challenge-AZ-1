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
# Web server environment using terraform
This challenge provides a hands-on experience in setting up a basic Azure environment using Terraform, a popular Infrastructure as Code (IaC) tool.

Participants will learn how to create a virtual network with multiple subnets, deploy virtual machines, and configure network security groups. Additionally, the challenge includes setting up essential infrastructure components like storage accounts and load balancers. By working through this challenge, students will gain practical skills in using Terraform to automate and manage cloud infrastructure, which is a crucial aspect of modern DevOps practices.

This challenge is ideal for those looking to deepen their understanding of Terraform and its application in real-world scenarios, making it a valuable addition to any DevOps curriculum.

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

<!-- TOC --><a name="network"></a>
### Network

- 1 VNet – 10.0.0.0/16
- 4 Subnets:
    - Application, Management, Backend, Web. All /24

<!-- TOC --><a name="compute"></a>
### Compute

- 2 Virtual Machines in an availability set running Linux (your choice of distro) in the web subnet
    - NSG allows SSH from management VM, allows web traffic from the Load Balancer. No external traffic
    - Script the installation of Apache
- 1 Virtual Machine running Linux (your choice of distro) in the Management subnet
    - NSG allows SSH from a single specific IP or network space only

<!-- TOC --><a name="supporting-infrastructure"></a>
### Supporting Infrastructure

- One storage account:
    - GRS Redundant
    - Only accessible to the VM in the Management subnet
    - One container “terraformstate”
    - One container “weblogs”
- One Load balancer that sends web traffic to the VMs in the availability set.
- One key vault