# Lab scenario

The organization has a web application that runs on a virtual machine in the on-premises data center. The organization wants to move all applications to the cloud but doesn't want to have a large number of servers to manage. We decide to evaluate Azure Container Instances and Docker.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/0631d220643c125d392b370b7e7b84da645ee6fe/11.%20Implement%20Azure%20Container%20Instances/arch%20diagram.png)

# Objective

- [x]Task 1: Deploy an Azure Container Instance using a Docker image.
- [x]Task 2: Test and verify deployment of an Azure Container Instance.

## 1) Deploy an Azure Container Instance using a Docker image.
 
In this task, we will create a simple web application using a Docker image. Docker is a platform that provides the ability to package and run applications in isolated environments called containers. Azure Container Instances provides the compute environment for the container image..

First, we'll create the container instance by giving in name and uploading the docker image

![Alt text](https://github.com/venuGanes/azure/blob/0631d220643c125d392b370b7e7b84da645ee6fe/11.%20Implement%20Azure%20Container%20Instances/1.1%20create%20container%20instanc.png)

Next, we'll create the dns label
![Alt text](https://github.com/venuGanes/azure/blob/0631d220643c125d392b370b7e7b84da645ee6fe/11.%20Implement%20Azure%20Container%20Instances/1.1.1%20dns%20label.png)

The image below shows the result of the container that was created
![Alt text](https://github.com/venuGanes/azure/blob/0631d220643c125d392b370b7e7b84da645ee6fe/11.%20Implement%20Azure%20Container%20Instances/1.1.2%20container%20name.png)

## 2) Test and verify deployment of an Azure Container Instance.

In this task, we review the deployment of the container instance. By default, the Azure Container Instance is accessible over port 80. After the instance has been deployed, we can navigate to the container using the DNS name that you provided in the previous task.

Once container created we'll copy the FQDN below
![Alt text](https://github.com/venuGanes/azure/blob/0631d220643c125d392b370b7e7b84da645ee6fe/11.%20Implement%20Azure%20Container%20Instances/2.2.1%20copy%20FQDN%20url.png)

Next, we'll paste the URL to the browser
![Alt text](https://github.com/venuGanes/azure/blob/0631d220643c125d392b370b7e7b84da645ee6fe/11.%20Implement%20Azure%20Container%20Instances/2.2.2%20fqdn%20url%20result.png)

Finally, we’ll check the logs once the browser is refreshed.
![Alt text](https://github.com/venuGanes/azure/blob/0631d220643c125d392b370b7e7b84da645ee6fe/11.%20Implement%20Azure%20Container%20Instances/2.2.3%20view%20logs.png)
