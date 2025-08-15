# scenario

The global organization plans to implement virtual networks. The immediate goal is to accommodate all the existing resources. However, the organization is in a growth phase and wants to ensure there is additional capacity for the growth.

The CoreServicesVnet virtual network has the largest number of resources. A large amount of growth is anticipated, so a large address space is necessary for this virtual network.

The ManufacturingVnet virtual network contains systems for the operations of the manufacturing facilities. The organization is anticipating a large number of internal connected devices for their systems to retrieve data from.

# Architecture Diagram
![Alt text]()

These virtual networks and subnets are structured in a way that accommodates existing resources yet allows for the projected growth.
Let's create these virtual networks and subnets to lay the foundation for our networking infrastructure.

# Objective

- [x]Task 1: Create a virtual network with subnets using the portal.
- [x]Task 2: Create a virtual network and subnets using a template.
- [x]Task 3: Create and configure communication between an Application Security Group and a Network Security Group.
- [x]Task 4: Configure public and private Azure DNS zones.

## 1) Create a virtual network with subnets using the portal.
 
The organization plans a large amount of growth for core services. 
In this task, we create the virtual network and the associated subnets to accommodate the existing resources and planned growth. In this task, we will use the Azure portal.


![Alt text]()

![Alt text]()



## 2) Create a virtual network and subnets using a template

In this task, we create the ManufacturingVnet virtual network and associated subnets. 
The organization anticipates growth for the manufacturing offices so the subnets are sized for the expected growth. For this task, we use a template to create the resources.



![Alt text]()

![Alt text]()

Make changes for the ManufacturingVnet virtual network



Make changes for the ManufacturingVnet subnets


Make changes to the parameters file

Deploy the custom template
![Alt text]()


## 3) Create and configure communication between an Application Security Group and a Network Security Group

In this task, we create an Application Security Group and a Network Security Group. The NSG will have an inbound security rule that allows traffic from the ASG. 
The NSG will also have an outbound rule that denies access to the internet.

Create the Application Security Group (ASG)
![Alt text]()

Create the Network Security Group and associate it with CoreServicesVnet

Configure an inbound security rule to allow ASG traffic

Configure an outbound NSG rule that denies Internet access





## 4) Configure public and private Azure DNS zones
In this task, we will create and configure public and private DNS zones.

##### Configure a public DNS zone
You can configure Azure DNS to resolve host names in the public domain. For example, if we purchased the contoso.xyz domain name from a domain name registrar, 
we can configure Azure DNS to host the contoso.com domain and resolve www.contoso.xyz to the IP address of the web server or web app.



##### Configure a private DNS zone
![Alt text]()


![Alt text]()


![Alt text]()



