# Lab scenario

The organization segments core IT apps and services (such as DNS and security services) from other parts of the business, including your manufacturing department. 
However, in some scenarios, apps and services in the core area need to communicate with those in the manufacturing area. 
In this lab, you configure connectivity between the segmented areas.
This is a common scenario for separating production from development or separating one subsidiary from another.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/8b20d047e70141ea6a653ee771bcf69f76d607d7/6.%20Implement%20Intersite%20Connectivity/arch%20diagram%20new.png)

# Objective

- [x] Task 1: Create a virtual machine in a virtual network.
- [x] Task 2: Create a virtual machine in a different virtual network.
- [x] Task 3: Use Network Watcher to test the connection between virtual machines.
- [x] Task 4: Configure virtual network peerings between different virtual networks.
- [x] Task 5: Use Azure PowerShell to test the connection between virtual machines.
- [x] Task 6: Create a custom route.

## 1) Create a virtual machine in a virtual network.
 
In this task, we create a core services virtual network with a virtual machine.

The image below shows the configuration of the virtual machine named CoreServicesVM.

![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/1.1%20create%20VM.png)

Next, the image shows the configuration of the virtual network named CoreServicesVnet and also the subnet specified below.
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/1.2%20CONFIGURE%20VIRTUAL%20NETWORK.png)



## 2)  Create a virtual machine in a different virtual network.

In this task, we create a manufacturing services virtual network with a virtual machine.

The image below shows the configuration of the virtual machine named ManufacturingVM and named the vnet as ManufacturingVnet.

![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/2.1%20create%20vm%20in%20another%20virtual%20network.png)

Also the subnets have been createad as below:

![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/2.2%20conf%20vnet%20subnet.png)

## 3) Use Network Watcher to test the connection between virtual machines

In this task, we verify that resources in peered virtual networks can communicate with each other. 
Network Watcher will be used to test the connection. Before continuing, we have to ensure both virtual machines have been deployed and are running.

![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/3.1%20network%20watcher%20connection%20t.shoot%20source%20type%20.png)

## 4) Configure virtual network peerings between different virtual networks.

In this task, we create a virtual network peering to enable communications between resources in the virtual networks.

Images below shows that both the virtual networks has beenn peered with each other.

![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/4.1%20peering%20corevnet%20to%20manvnet%20cont.png)
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/4.1%20peering%20corevnet%20to%20manvnet.png)
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/4.2%20connected.png)
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/4.2%20manvnet%20peering.png)
## 5) Use Azure PowerShell to test the connection between virtual machines.
In this task, we retest the connection between the virtual machines in different virtual networks.

##### Verify the private IP address of the CoreServicesVM
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/5.1%20verify%20priv%20ip%20add.png)
##### Test the connection to the CoreServicesVM from the ManufacturingVM.
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/5.2%20run%20script%20to%20test%20connection.png)
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/5.2%20output.png)


## 6) Create a custom route.

In this task, we want to control network traffic between the perimeter subnet and the internal core services subnet. 
A virtual network appliance will be installed in the core services subnet and all traffic should be routed there.

First we'll add subnets to CoreServicesVnet
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/6.1%20add%20subnet%20to%20coreservicesvnet.png)

Next, create the route table
![Alt text][(](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/6.2%20create%20routetable.png))
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/6.3%20add%20route.png)

The route has been added as shown below:
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/6.3%20routeadded.png)

and we'll associate it
![Alt text](https://github.com/venuGanes/azure/blob/4b20c99d551140686f2233e8acec1846513530bf/6.%20Implement%20Intersite%20Connectivity/6.4%20associate%20subnet.png)
