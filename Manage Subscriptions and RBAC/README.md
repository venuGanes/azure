# scenario

To simplify the management of Azure resources in the organization, I've been tasked with implementing the following functionality:

Creating a management group that includes all Azure subscriptions.

Granting permissions to submit support requests for all subscriptions in the management group. The permissions should be limited only to:

- [x] Create and manage virtual machines
- [x] Create support request tickets 

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/3175824e654315657f845250c250d6916b7050a0/Manage%20Subscriptions%20and%20RBAC/3.%20arch%20diagram%201.png)

# Objective

- [x] Implement management groups
- [x] Review and assign a built-in Azure role
- [x] Create a custom RBAC role
- [x] Monitor role assignments with the Activity log.

## 1) Implement management groups
 
In this task, I was responsible for creating and configuring management groups in Azure. These groups help organize and segment subscriptions logically, making it easier to apply role-based access control (RBAC) and Azure Policies. By using management groups, I can assign permissions and policies that automatically apply to all associated subscriptions. For instance, in a scenario where a support team needs access to multiple subscriptions (like in Europe), grouping those under a single management group simplifies access without needing to configure each subscription individually. In my case, this setup allows the Help Desk team to create support requests across all subscriptions efficiently.

Created a management group as such:

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/5.create%20management%20group.png)

After creation:

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/5.1%20create%20management%20group.png)


## 2) Review and assign a built-in Azure role

In this task, we'll review the built-in roles and assign the VM Contributor role to a member of the Help Desk. The VM contributor role lets us manage virtual machines but not access the OS or manage the virtual network and storage account they are connected to.

The below image shows the member of Helpdesk IT has been assigned under the role of Helpdesk IT

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/6.1%20task%202%20add%20role%20assignment.png)
![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/6.2%20task%202%20select%20member.png)

Review after role assignment:

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/6.3%20task%202%20CREATED.png)

## 3) Create a custom RBAC role

In this task, I've created a custom RBAC role. Custom roles are a core part of implementing the principle of least privilege for an environment.

The image below shows a custom role being created with specific permissions excluded. These exclusions are necessary because Azure resource providers collections of REST API operations that enable various Azure services (like managing storage or virtual machines) grant powerful capabilities. Since the Help Desk team does not require such access, these permissions are intentionally removed during the role cloning process to maintain proper security and limit unnecessary control.

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/7.1%20task%203.png)

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/7.%20task%203%20CONT%201%20permission.png)

## 4)  Monitor role assignments with the Activity log

In this task, we view the activity log to determine if anyone has created a new role.

We've located to the "Az104-mg153731133' resource and selected the activity log as shown below shows the result:

![Alt text](https://github.com/venuGanes/azure/blob/2bc6de069a1ae75ae27c435f4a9722a0cea60a8b/Manage%20Subscriptions%20and%20RBAC/8.1%20task%204%20.png)
