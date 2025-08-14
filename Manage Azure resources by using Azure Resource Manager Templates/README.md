# scenario

We are exploring ways to automate and simplify resource deployment. The organization is seeking ways to reduce administrative overhead, minimize human error, and enhance consistency.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/arch%20diagram%20new.png)

# Objective

- [x]Task 1: Create an Azure Resource Manager template.
- [x]Task 2: Edit an Azure Resource Manager template and redeploy the template.
- [x]Task 3: Configure the Cloud Shell and deploy a template with Azure PowerShell.
- [x]Task 4: Deploy a template with the CLI.
- [x]Task 5: Deploy a resource by using Azure Bicep.

## 1) Create an Azure Resource Manager template.
 
In this task, we will create a managed disk in the Azure portal. Managed disks are storage designed to be used with virtual machines. Once the disk is deployed, we will export a template that we can use in other deployments.

The image below shows the disk creation with the following configurations: 
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/1.%201%20creating%20disk.png)

The image below shows the exported template for disk creation, which will simplify future disk creation tasks.
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/1.%202%20export%20template%20.png)



## 2) Edit an Azure Resource Manager template and redeploy the template.

In this task, we use the downloaded template to deploy a new managed disk. This task outlines how to quickly and easily repeat deployments.

The image below shows a custom deployment where we load the template and use the editor to modify the file. Here, we've made changes to the underlined items.

![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/2.1%20edit%20template.png)

![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/2.2%20edit%20parmeter%20file.png)

Once we've made the changes, notice that two disk files are created.
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/2.3%20two%20disk%20created.png)


## 3) Configure the Cloud Shell and deploy a template with Azure PowerShell.

In this task, we work with the Azure Cloud Shell and Azure PowerShell. Azure Cloud Shell is an interactive, authenticated, browser-accessible terminal for managing Azure resources. It provides the flexibility of choosing the shell experience that best suits the way we work, either Bash or PowerShell. In this task, we use PowerShell to deploy a template.

The image below shows that we're using the classic version of PowerShell.
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/3.2%20upload%20both%20downloaded%20templates.png)

The image below shows the template that is being edited in order to deploy.
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/3.3%20editing%20templat%20files.png)

Once we've saved the changes made to the template, we'll proceed with deploying it as below:
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/3.4%20deeploying%20resource%20group.png)

To confirm if the disk was created, we'll use the command "Get-AzDisk" as below:
![Alt text](https://github.com/venuGanes/azure/blob/a223a3ec95b9c0b9a82bb0d92cc53a22e0d9e14c/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/3.5%20deployment%20succeeded.png)



## 4) Deploy a template with the CLI.

The image below shows that we're using Bash.
![Alt text](https://github.com/venuGanes/azure/blob/4acf35abcccb160d04f03485aa67b804a3ddf482/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/4.2%20editing%20and%20deploying%20in%20bash.png)

The image below shows the template that is being edited in order to deploy.
![Alt text](https://github.com/venuGanes/azure/blob/4acf35abcccb160d04f03485aa67b804a3ddf482/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/4.2%20editing%20and%20deploying%20in%20bash.png)

Once we've saved the changes made to the template, we'll proceed with deploying it as below:
![Alt text](https://github.com/venuGanes/azure/blob/4acf35abcccb160d04f03485aa67b804a3ddf482/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/4.3%20using%20cli%20deployment%20scceeded.png)


## 5) Deploy a resource by using Azure Bicep.

In this task, we will use a Bicep file to deploy a managed disk. Bicep is a declarative automation tool that is built on ARM templates.

The image below shows the bicep template being edited in order to deploy.

![Alt text](https://github.com/venuGanes/azure/blob/4acf35abcccb160d04f03485aa67b804a3ddf482/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/5.1%20Editing%20the%20Bicep%20file.png)

Once we've saved the changes made to the template, we'll proceed with deploying it as below:
![Alt text](https://github.com/venuGanes/azure/blob/4acf35abcccb160d04f03485aa67b804a3ddf482/Manage%20Azure%20resources%20by%20using%20Azure%20Resource%20Manager%20Templates/5.2%20Deployment%20succeeded.png)


