# Lab scenario

The organization has a public website. We need to load balance incoming public requests across different virtual machines. We also need to provide images and videos from different virtual machines. We plan on implementing an Azure Load Balancer and an Azure Application Gateway. All resources are in the same region.

# Objective

- [x] Task 1: Use a template to provision an infrastructure.
- [x] Task 2: Configure an Azure Load Balancer.
- [x] Task 3: Configure an Azure Application Gateway.

## 1) Use a template to provision an infrastructure.
 In this task, we will use a template to deploy one virtual network, one network security group, and three virtual machines.

First, we'll begin with creating the load balancer:

![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/1.1%20task%201%20custom%20deployment.png)

Next, 
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.2%20frontend%20ip%20conf.png)



## 2)  Configure an Azure Load Balancer.
In this task, we implement an Azure Load Balancer in front of the two Azure virtual machines in the virtual network. Load Balancers in Azure provide layer 4 connectivity across resources, such as virtual machines. Load Balancer configuration includes a front-end IP address to accept connections, a backend pool, and rules that define how connections should traverse the load balancer.

#### Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.%20task%202%20arch%20diagram%20LB.png)

The image below shows the configuration of a load balancer, including the front-end IP configuration, the addition of a public IP address, and the backend pool.

![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.1%20task%202.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.2%20frontend%20ip%20conf.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.3%20add%20public%20add.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.4%20backend%20pool%20conf.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.4%20backend%20pool%20conf%20cont.png)

Add a rule to determine how incoming traffic is distributed

![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/2.5%20traffic%20rule.png)

## 3) Configure an Azure Application Gateway.
In this task, we implement an Azure Application Gateway in front of two Azure virtual machines. An Application Gateway provides layer 7 load balancing, Web Application Firewall (WAF), SSL termination, and end-to-end encryption to the resources defined in the backend pool. The Application Gateway routes images to one virtual machine and videos to the other virtual machine.

#### Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/3.%20task%203%20Architecture%20diagram%20-%20Application%20Gateway.png)

The image below shows the configuration of the virtual network along with subnet

![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/3.1%20add%20subnet.png)


![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/3.2%20app%20gateway%20creation%20conf.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/3.2%20app%20gateway%20creation.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/3.3%20backend%20pool.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/3.4%20adding%20routing%20table.png)
![Alt text](https://github.com/venuGanes/azure/blob/7f11fca42e362d2728f7fa7d87a3725da695fbef/7.%20Implement%20Network%20Traffic%20Management/3.4%20path%20rules.png)
