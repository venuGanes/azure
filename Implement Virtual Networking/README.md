# scenario

The global organization plans to implement virtual networks. The immediate goal is to accommodate all the existing resources. However, the organization is in a growth phase and wants to ensure there is additional capacity for the growth.

The CoreServicesVnet virtual network has the largest number of resources. A large amount of growth is anticipated, so a large address space is necessary for this virtual network.

The ManufacturingVnet virtual network contains systems for the operations of the manufacturing facilities. The organization is anticipating a large number of internal connected devices for their systems to retrieve data from.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/arch%20diagram%20new.png)

These virtual networks and subnets are structured in a way that accommodates existing resources yet allows for the projected growth.
Let's create these virtual networks and subnets to lay the foundation for our networking infrastructure.

# Objective

- [x] Task 1: Create a virtual network with subnets using the portal.
- [x] Task 2: Create a virtual network and subnets using a template.
- [x] Task 3: Create and configure communication between an Application Security Group and a Network Security Group.
- [x] Task 4: Configure public and private Azure DNS zones.

## 1) Create a virtual network with subnets using the portal.
 
The organization plans a large amount of growth for core services. 
In this task, we create the virtual network and the associated subnets to accommodate the existing resources and planned growth. In this task, we will use the Azure portal.

First, we started off with creating a virtual network as below:
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/1.1%20create%20vn.png)

Next, configured with ip address and subnet address"SharedServicesSubnet" & "DatabaseSubnet" as below:
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/1.2%20create%20vn%20(ip%20add%20and%20subnet).png)

Image shows the subnet has been created
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/1.3%20subnets%20created.png)

Finally, we'll export the template to create "ManufacturingVnet" in the later task. 
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/1.4%20download%20template.png)

## 2) Create a virtual network and subnets using a template

In this task, we create the ManufacturingVnet virtual network and associated subnets. 
The organization anticipates growth for the manufacturing offices so the subnets are sized for the expected growth. For this task, we use a template to create the resources.

Before we begin, we will review the original template.json file below:

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/2.1%20make%20cchanges%20to%20coreservicsvnet%20(before).png)

Next, we'll make changes to the ip and Vnet for the ManufacturingVnet virtual network as below:

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/2.1%20make%20cchanges%20to%20coreservicsvnet%20%20(after).png)


Next, we'll make changes for the ManufacturingVnet subnets

Before:
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/2.2%20Make%20changes%20for%20the%20ManufacturingVnet%20subnets%20(before).png)

After:
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/2.2%20Make%20changes%20for%20the%20ManufacturingVnet%20subnets%20(after).png)

Next, we'll make changes to the parameters file
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/1.3%20make%20changes%20to%20parameter%20file.png)

Deploy the custom template
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/1.4%20deploy%20the%20custom%20template.png)


## 3) Create and configure communication between an Application Security Group and a Network Security Group

In this task, we create an Application Security Group and a Network Security Group. The NSG will have an inbound security rule that allows traffic from the ASG. 
The NSG will also have an outbound rule that denies access to the internet.

Create the Application Security Group (ASG)
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.1%20Create%20the%20Application%20Security%20Group%20(ASG).png)

Create the Network Security Group and associate it with CoreServicesVnet
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.2%20Create%20the%20Network%20Security%20Group%20and%20associate%20it%20with%20CoreServicesVnet.png)
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.2.1%20Create%20the%20Network%20Security%20Group%20and%20associate%20it%20with%20CoreServicesVnet%20(associate).png)

Configure an inbound security rule to allow ASG traffic
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.3%20add%20inbound%20rule.png)
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.3%20add%20inbound%20rule%20cont.png)
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.3%20add%20inbound%20rule%20cont%201.png)

Configure an outbound NSG rule that denies Internet access
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.4%20add%20outboubd%20rule.png)
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.3%20add%20inbound%20rule%20cont.png)
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/3.4%20add%20outboubd%20rule%20cont%201.png)




## 4) Configure public and private Azure DNS zones
In this task, we will create and configure public and private DNS zones.

##### Configure a public DNS zone
We can configure Azure DNS to resolve host names in the public domain. For example, if we purchased the contoso.xyz domain name from a domain name registrar, 
we can configure Azure DNS to host the contoso.com domain and resolve www.contoso.xyz to the IP address of the web server or web app.

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/4.1%20dns%20zone.png)
![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/4.2%20recordset%20ceation.png)

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/4.2%20recordset%20ceation%20result.png)

##### Configure a private DNS zone

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/4.3%20create%20private%20dns%20zone.png)

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/4.3%20create%20private%20dns%20zone%20created.png)

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/4.4%20configure%20virtual%20network%20link.png)

![Alt text](https://github.com/venuGanes/azure/blob/8674789eb1b277e1df6d3084614b10800610a32c/Implement%20Virtual%20Networking/4.5%20add%20record%20set.png)

