# Lab scenario

Your organization segments core IT apps and services (such as DNS and security services) from other parts of the business, including your manufacturing department. 
However, in some scenarios, apps and services in the core area need to communicate with apps and services in the manufacturing area. 
In this lab, you configure connectivity between the segmented areas.
This is a common scenario for separating production from development or separating one subsidiary from another.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/c381f7b2fd85a8c2dc77d35307a7b213b413ab84/Manage%20Microsoft%20Entra%20ID%20Identities%20(Requires%20MFA%20)/3.1%20architecture%20diagram%201.png)

# Objective

- [x] Task 1: Create a virtual machine in a virtual network.
- [x] Task 2: Create a virtual machine in a different virtual network.
- [x] Task 3: Use Network Watcher to test the connection between virtual machines.
- [x] Task 4: Configure virtual network peerings between different virtual networks.
- [x] Task 5: Use Azure PowerShell to test the connection between virtual machines.
- [x] Task 6: Create a custom route.

## 1) Create a virtual machine in a virtual network.
 
In this task, you create a core services virtual network with a virtual machine.

![Alt text]()

## 2)  Create a virtual machine in a different virtual network.te groups and add members

In this task, you create a manufacturing services virtual network with a virtual machine.

In this task, you create a manufacturing services virtual network with a virtual machine.
![Alt text]()

![Alt text]()


## 3) Use Network Watcher to test the connection between virtual machines

In this task, you verify that resources in peered virtual networks can communicate with each other. 
Network Watcher will be used to test the connection. Before continuing, ensure both virtual machines have been deployed and are running.



## 4) Configure virtual network peerings between different virtual networks.

In this task, you create a virtual network peering to enable communications between resources in the virtual networks.

## 5) Use Azure PowerShell to test the connection between virtual machines.
In this task, you retest the connection between the virtual machines in different virtual networks.

##### Verify the private IP address of the CoreServicesVM
##### Test the connection to the CoreServicesVM from the ManufacturingVM.


## 6) Create a custom route.

In this task, you want to control network traffic between the perimeter subnet and the internal core services subnet. 
A virtual network appliance will be installed in the core services subnet and all traffic should be routed there.

