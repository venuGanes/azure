# Lab scenario

Your organization has a public website. You need to load balance incoming public requests across different virtual machines. You also need to provide images and videos from different virtual machines. You plan on implementing an Azure Load Balancer and an Azure Application Gateway. All resources are in the same region.

# Architecture Diagram
![Alt text]()

# Objective

- [x] Task 1: Use a template to provision an infrastructure.
- [x] Task 2: Configure an Azure Load Balancer.
- [x] Task 3: Configure an Azure Application Gateway.

## 1) Use a template to provision an infrastructure.
 In this task, you will use a template to deploy one virtual network, one network security group, and three virtual machines.


![Alt text]()

![Alt text]()



## 2)  Configure an Azure Load Balancer.
In this task, you implement an Azure Load Balancer in front of the two Azure virtual machines in the virtual network. Load Balancers in Azure provide layer 4 connectivity across resources, such as virtual machines. Load Balancer configuration includes a front-end IP address to accept connections, a backend pool, and rules that define how connections should traverse the load balancer.


![Alt text]()
Add a rule to determine how incoming traffic is distributed

![Alt text]()

## 3) Configure an Azure Application Gateway.
In this task, you implement an Azure Application Gateway in front of two Azure virtual machines. An Application Gateway provides layer 7 load balancing, Web Application Firewall (WAF), SSL termination, and end-to-end encryption to the resources defined in the backend pool. The Application Gateway routes images to one virtual machine and videos to the other virtual machine.

![Alt text]()

