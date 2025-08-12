# scenario

To simplify the management of Azure resources in the organization, I've been tasked with implementing the following functionality:

Creating a management group that includes all Azure subscriptions.

Granting permissions to submit support requests for all subscriptions in the management group. The permissions should be limited only to:

- [x] Create and manage virtual machines
- [x] Create support request tickets 

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/3175824e654315657f845250c250d6916b7050a0/Manage%20Subscriptions%20and%20RBAC/3.%20arch%20diagram%201.png)

# Objective

- [x] Create and configure user accounts
- [x] Create groups and add members

## 1) Create and configure user accounts
 
User has been created and has been named as "az104-user1"

![Alt text](https://github.com/venuGanes/azure/blob/3e4d9f26f8fb60aea2ccb2e97ff26d5d9019acb2/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/4.2%20user%20details.png)


Invite an external user has been created and has been named as "venu"

Configuration as below:

![Alt text](https://github.com/venuGanes/azure/blob/6848d50e25a3d86609c0427f4122f579d873ef74/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/4.31%20invite%20external%20user.png)

![Alt text](https://github.com/venuGanes/azure/blob/6848d50e25a3d86609c0427f4122f579d873ef74/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/4.32%20invite%20external%20user.png)

Result after creation, received via outlook

![Alt text](https://github.com/venuGanes/azure/blob/6848d50e25a3d86609c0427f4122f579d873ef74/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/4.32%20invitation%20message.png)

## 2)  Create groups and add members

For this task, we create a group account named " IT Lab Administrator". And  we'll add the member/user and the guest user to the group as shown below:
![Alt text](https://github.com/venuGanes/azure/blob/b6ef40b3d5fa69088d8e9ba90eace27d8fbc4a4d/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/4.41%20group%20created.png)


![Alt text](https://github.com/venuGanes/azure/blob/b6ef40b3d5fa69088d8e9ba90eace27d8fbc4a4d/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/4.4%20adding%20member%20to%20group.png)

