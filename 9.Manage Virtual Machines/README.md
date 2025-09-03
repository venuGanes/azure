# Lab scenario

Your organization wants to explore deploying and configuring Azure virtual machines. First, you implement an Azure virtual machine with manual scaling. Next, you implement a Virtual Machine Scale Set and explore autoscaling.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/f62f71a3b59ab040ff634ad0b6836229f00b0980/8.Manage%20Azure%20Storage/arch%20diagram%201.png)

# Objective

- [x]Task 1: Deploy zone-resilient Azure virtual machines by using the Azure portal.
- [x]Task 2: Manage compute and storage scaling for virtual machines.
- [x]Task 3: Create and configure Azure Virtual Machine Scale Sets.
- [x]Task 4: Scale Azure Virtual Machine Scale Sets.
- [x]Task 5: Create a virtual machine using Azure PowerShell (optional 1).
- [x]Task 6: Create a virtual machine using the CLI (optional 2).
- 
## 1) Deploy zone-resilient Azure virtual machines by using the Azure portal
 
In this task, you will deploy two Azure virtual machines into different availability zones by using the Azure portal. Availability zones offer the highest level of uptime SLA for virtual machines at 99.99%. To achieve this SLA, you must deploy at least two virtual machines across different availability zones.

![Alt text]

## 2) Manage compute and storage scaling for virtual machines

In this task, you will scale a virtual machine by adjusting its size to a different SKU. Azure provides flexibility in VM size selection so that you can adjust a VM for periods of time if it needs more (or less) compute and memory allocated. This concept is extended to disks, where you can modify the performance of the disk, or increase the allocated capacity.

##### 2.1 Azure Virtual Machine Scale Sets Architecture Diagram

Here, we'll add a container named data with a data policy type of Time-based retention which is set to 180 days. With a time-based retention policy, users can set policies to store data for a specified interval. When a time-based retention policy is set, objects can be created and read, but not modified or deleted. After the retention period has expired, objects can be deleted but not overwritten.

![Alt text]

##### 2.2 Azure Virtual Machine Scale Sets Architecture Diagram

###### Scale out rule

###### Scale in rule


###### Set the instance limits


## 3) Create and configure Azure Virtual Machine Scale Sets

In this task, you will deploy an Azure virtual machine scale set across availability zones. VM Scale Sets reduce the administrative overhead of automation by enabling you to configure metrics or conditions that allow the scale set to horizontally scale, scale in or scale out.

## 4) Create a virtual machine using Azure PowerShell (option 1)

In this task, you scale the virtual machine scale set using a custom scale rule.

## 5) Create a virtual machine using the CLI (option 2)

