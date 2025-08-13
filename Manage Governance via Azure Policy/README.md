# scenario

Your organization's cloud footprint has expanded significantly over the last year. During a recent audit, you discovered a substantial number of resources that do not have a defined owner, project, or cost center. In order to improve the management of Azure resources in your organization, you decide to implement the following functionality:

- [x] Apply resource tags to attach important metadata to Azure resources

- [x] Enforce the use of resource tags for new resources by using Azure policy

- [x] Update existing resources with resource tags

- [x] Use resource locks to protect configured resources



# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/arch%20diagram%20new.png)

# Objective

- [x]Task 1: Create and assign tags via the Azure portal.
- [x]Task 2: Enforce tagging via an Azure Policy.
- [x]Task 3: Apply tagging via an Azure Policy.
- [x]Task 4: Configure and test resource locks.
- 

## 1) Apply resource tags to attach important metadata to Azure resources
 
In this task, we will create and assign a tag to an Azure resource group via the Azure portal. Tags are a critical component of a governance strategy as outlined by the Microsoft Well-Architected Framework and Cloud Adoption Framework. Tags can allow you to quickly identify resource owners, sunset dates, group contacts, and other name/value pairs that organization deems important. For this task, we'll assign a tag identifying the resource Cost Center.

We've created a resource group with the name "az104-rg2" and also tag named "Cost Center" as below: 
![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/1.1%20Create%20resource%20group.png)

![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/1.2%20Create%20tags.png)

After creation:

![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/1.3%20created%20resource%20group.png)

## 2)Enforce the use of resource tags for new resources by using Azure policy

In this task, we will assign the built-in Require a tag and its value on the resources policy to the resource group and evaluate the outcome. Azure Policy can be used to enforce configuration, and in this case, governance, to your Azure resources.

##### At the beginning of this task we've selected a policy called "Require a tag and its value on resources" that Enforces a required tag and its value and Does not apply to the resources group

![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/2.1%20selecting%20policy%20defiintion.png)
![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/2.2%20definition%20selecting%20policy%20defiintion.png)

The following task we'll assign the policy by selecting the appropriate tag vallue and resource group.

![Alt text]
(https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/2.3%20Assign%20policy%20selecting%20resource%20group.png)
![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/2.4%20Assign%20policy%20selecting%20set%20parameters%20for%20tag.png)
![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/2.5%20Review.png)

Lastly, we'll create a storage account

![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/2.6%20Create%20storage%20account.png)
![Alt text](https://github.com/venuGanes/azure/blob/fe55a5100a2b6b23501258d904c618bab33e24f9/Manage%20Governance%20via%20Azure%20Policy/2.7%20Storage%20account%20created.png)


## 3) Update existing resources with resource tags

In this task, we will use the new policy definition to remediate any non-compliant resources. In this scenario, we will make any child 
resources of a resource group inherit the Cost Center tag that was defined on the resource group.

![Alt text]()

![Alt text]()
![Alt text]()
![Alt text]()
![Alt text]()


## 4)  Use resource locks to protect configured resources

In this task, we configure and test a resource lock. Locks prevent either deletions or modifications of a resource.
![Alt text]()
![Alt text]()
![Alt text]()



