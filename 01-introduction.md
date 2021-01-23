# Azure Kubernetes Service on Azure Stack HCI

Azure Kubernetes Service on Azure Stack HCI is an on-premises implementation of the popular Azure Kubernetes Service (AKS) orchestrator, which automates running containerized applications at scale. Azure Kubernetes Service is now in preview on Azure Stack HCI and on Windows Server 2019 Datacenter, making it quicker to get started hosting Linux and Windows containers in your datacenter.


Creates new Azure VM and install prerequisites to run Proof of Concept for Azure Stack HCI.

## Use AKS to automate management of containerized applications

Here's some of the functionality provided by Azure Kubernetes Service while in preview on Azure Stack HCI:

* Deploy containerized apps at scale to Kubernetes clusters running across the Azure Stack HCI cluster
* Deploy and manage both Linux and Windows-based containerized apps
* Deploy AKS on Azure Stack HCI using Windows Admin Center or PowerShell
* Scale up or down by adding or removing nodes to the Kubernetes cluster
* Manage storage and networking on your Kubernetes cluster
* Provide automatic updates for your Kubernetes deployment
* Upgrade to the latest available Kubernetes version
* Use the popular Azure services through Azure Arc for Kubernetes

## Simplify setting up Kubernetes

Azure Kubernetes Service simplifies the process of setting up Kubernetes on Azure Stack HCI and Windows Server 2019 Datacenter, and includes the following features:

* A Windows Admin Center wizard for setting up Kubernetes and its dependencies (such as kubeadm, kubelet, kubectl, and a pod network add-on)
* A Windows Admin Center wizard for creating Kubernetes clusters to run your containerized applications
* PowerShell cmdlets for setting up Kubernetes and creating Kubernetes clusters, in case you'd rather script the host setup and Kubernetes cluster creation

## View and manage Kubernetes using on-premises tools or Azure Arc

Once you've set up Azure Kubernetes Service on-premises and created a Kubernetes cluster, we provide a couple ways to manage and monitor your Kubernetes infrastructure:

* On-premises using popular tools like Kubectl and Kubernetes dashboard - Use an open-source, web-based interface to deploy applications to a Kubernetes cluster, manage cluster resources, troubleshoot, and view running applications.

* In the Azure portal using Azure Arc - Use Azure Arc to manage applications deployed on top of Kubernetes clusters across your cloud and on-premises environments.
Azure Arc also enables you to manage your Kubernetes clusters with other Azure services including:

    * Azure Monitor
    * Azure Policy
    * Role-Based Access Control

## Where can I run Azure Kubernetes Service?
Azure Kubernetes Service is available on the following platforms:

* In the Azure cloud via [Azure Kubernetes Service in Azure](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-prepare-app)
* On-premises via [Azure Kubernetes Service on Azure Stack HCI](02-aks-on-azure-stack-hci.md#L1)
* On-premises via Azure Kubernetes Service runtime on Windows Server 
* On-premises in an Azure Stack Hub environment using the AKS engine on Azure Stack Hub.

## How does Kubernetes work on Azure Stack HCI?
Azure Kubernetes Service works a little differently when run on Azure Stack HCI than when using it in the Azure cloud:

* The Kubernetes service in Azure is a hosted service where much of the Kubernetes management infrastructure (control plane) is managed for you. Both the control plane and your containerized applications run in Azure virtual machines.
* With Azure Kubernetes Service on Azure Stack HCI, you set up the service directly on your Azure Stack HCI cluster, putting you in control of the control plane, so to speak. The control plane, your containerized applications, and Azure Kubernetes Service itself all run in virtual machines hosted by your hyperconverged cluster.

Once Azure Kubernetes Service is set up on your Azure Stack HCI cluster, it works similarly to the hosted Azure Kubernetes Service: you use the service to create Kubernetes clusters that run your containerized applications. These Kubernetes clusters are groups of VMs that act as worker nodes, running your application containers. The Kubernetes cluster also contains a control plane, which consists of Kubernetes system services used to orchestrate the application containers.

## Step by Step Installation and Configuration

* Install using Powershell
* Install on WAC (Windows Admin Center)

## Hands-on Labs

* Configure K8s on Win 10 using Docker desktop and register it to Azure ARC
* Deploy a sample App on AKS-HCI using GitOps integration
* Policy definition and deployment to all instances

## Troubleshooting

* **kubectl** usage for investigation
* Log file(s) analysis
* **Azure Monitor** usage

## Resources

### [Azure Stack HCI documentation](https://docs.microsoft.com/en-us/azure-stack/hci/)

### [System requirements for Azure Kubernetes Service on Azure Stack HCI](https://docs.microsoft.com/en-us/azure-stack/aks-hci/system-requirements)

### Support Statement

This solution is not officially support by **Microsoft** and experimental, may not work in the future.

 > Yagmur Sahin
 >
 > Twitter: [@yagmurs](https://twitter.com/yagmurs)
