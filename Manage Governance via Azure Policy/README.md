# scenario

Your organization's cloud footprint has expanded significantly over the last year. During a recent audit, you discovered a substantial number of resources that do not have a defined owner, project, or cost center. In order to improve the management of Azure resources in your organization, you decide to implement the following functionality:

- [x] Apply resource tags to attach important metadata to Azure resources

- [x] Enforce the use of resource tags for new resources by using Azure policy

- [x] Update existing resources with resource tags

- [x] Use resource locks to protect configured resources



# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/3175824e654315657f845250c250d6916b7050a0/Manage%20Subscriptions%20and%20RBAC/3.%20arch%20diagram%201.png)

# Objective

- [x]Task 1: Create and assign tags via the Azure portal.
- [x]Task 2: Enforce tagging via an Azure Policy.
- [x]Task 3: Apply tagging via an Azure Policy.
- [x]Task 4: Configure and test resource locks.
- 

## 1) Apply resource tags to attach important metadata to Azure resources
 
In this task, you will create and assign a tag to an Azure resource group via the Azure portal. Tags are a critical component of a governance strategy as outlined by the Microsoft Well-Architected Framework and Cloud Adoption Framework. Tags can allow you to quickly identify resource owners, sunset dates, group contacts, and other name/value pairs that your organization deems important. For this task, you assign a tag identifying the resource Cost Center.

Created management group as such:

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/5.create%20management%20group.png)

After creation:

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/5.1%20create%20management%20group.png)


## 2)Enforce the use of resource tags for new resources by using Azure policy

In this task, you will assign the built-in Require a tag and its value on the resources policy to the resource group and evaluate the outcome. Azure Policy can be used to enforce configuration, and in this case, governance, to your Azure resources.

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/6.1%20task%202%20add%20role%20assignment.png)
![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/6.2%20task%202%20select%20member.png)

Review after role assignment:

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/6.3%20task%202%20CREATED.png)

## 3) Update existing resources with resource tags

In this task, we will use the new policy definition to remediate any non-compliant resources. In this scenario, we will make any child 
resources of a resource group inherit the Cost Center tag that was defined on the resource group.

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/7.1%20task%203.png)

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/7.%20task%203%20CONT%201%20permission.png)

## 4)  Use resource locks to protect configured resources

In this task, you configure and test a resource lock. Locks prevent either deletions or modifications of a resource.


![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/8.1%20task%204%20.png)

