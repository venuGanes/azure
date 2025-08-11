# Lab scenario

My organization is setting up a new training environment for onboarding new software developers. This environment will be used to practice deploying and troubleshooting cloud-based applications. Several trainers and mentors will be assigned to oversee the training labs, including managing the cloud resources. To allow them to sign in securely using Microsoft Entra ID, I have been tasked with creating and configuring the necessary user accounts and role-based groups. To reduce manual management, I have configured the groups so that membership updates automatically based on each user’s department and role.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/c381f7b2fd85a8c2dc77d35307a7b213b413ab84/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/3.1%20architecture%20diagram%201.png)

# Objective
- [x] Create and configure user accounts
- [x]Create groups and add members

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

