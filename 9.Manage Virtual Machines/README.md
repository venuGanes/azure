# Lab scenario

The organization is currently storing data in on-premises data stores. Most of these files are not accessed frequently. 
We would like to minimize the cost of storage by placing infrequently accessed files in lower-priced storage tiers. 
We also plan to explore different protection mechanisms that Azure Storage offers, including network access, authentication, authorization, and replication.
Finally, we want to determine to what extent Azure Files is suitable for hosting on-premises file shares.

# Architecture Diagram
![Alt text](https://github.com/venuGanes/azure/blob/f62f71a3b59ab040ff634ad0b6836229f00b0980/8.Manage%20Azure%20Storage/arch%20diagram%201.png)

# Objective
- [x]Task 1: Create and configure a storage account.
- [x]Task 2: Create and configure secure blob storage.
- [x]Task 3: Create and configure secure Azure file storage.

## 1) Create and configure a storage account.
 
In this task, we will create and configure a storage account. The storage account will use geo-redundant storage and will not have public access.

![Alt text](https://github.com/venuGanes/azure/blob/f62f71a3b59ab040ff634ad0b6836229f00b0980/8.Manage%20Azure%20Storage/1.1%20creating%20storage%20account.png)

Next, we'll create a rule for the storage

##### Create a rule name movetocool
![Alt text](https://github.com/venuGanes/azure/blob/af339442aa44344b1a97e8c26732fa8653b7e245/8.Manage%20Azure%20Storage/2.1%20task%202%20%20cont%20img%201st.png)

![Alt text](https://github.com/venuGanes/azure/blob/07f100fa14a6ed69634a9dc3d226143c3b0ede3b/8.Manage%20Azure%20Storage/2.1%20task%202%20%20cont%20img%20created.png)

## 2) Create and configure secure blob storage.

In this task, we will create a blob container and upload an image. Blob containers are directory-like structures that store unstructured data.

##### 2.1 Create a blob container and a time-based retention policy

Here, we'll add a container named data with a data policy type of Time-based retention which is set to 180 days. With a time-based retention policy, users can set policies to store data for a specified interval. When a time-based retention policy is set, objects can be created and read, but not modified or deleted. After the retention period has expired, objects can be deleted but not overwritten.

![Alt text](https://github.com/venuGanes/azure/blob/af339442aa44344b1a97e8c26732fa8653b7e245/8.Manage%20Azure%20Storage/2.1%20task%202%20%20cont%20img.png)
![Alt text](https://github.com/venuGanes/azure/blob/8141524fbfe3fdc31c37653e5d759b65c25e5ed5/8.Manage%20Azure%20Storage/2.2%20Immutable%20blob%20storage.png)

##### 2.2 Manage blob uploads

In this task, we'll upload the blob/file and access tier is set to Hot (A tier optimized for storing data that is accessed or modified frequently. And also it'll be uploaded to a folder named security test

![Alt text](https://github.com/venuGanes/azure/blob/8141524fbfe3fdc31c37653e5d759b65c25e5ed5/8.Manage%20Azure%20Storage/2.3%20upload%20blob.png)
![Alt text]()
##### 2.3 Configure limited access to the blob storage

First, we'll select the Genrate SAS option available next to the file we uploaded and set the permission to read and save it. After that, once we've saved it we'll be able to see the "Generate SAS token and URL" and copy the "Blob SAS URL" and paste it to the browser, we'll be able to see the content of the file. 
![Alt text](https://github.com/venuGanes/azure/blob/8141524fbfe3fdc31c37653e5d759b65c25e5ed5/8.Manage%20Azure%20Storage/2.3.1%20image%20uploaded%20to%20foled%20security%20test.png)
![Alt text](https://github.com/venuGanes/azure/blob/8141524fbfe3fdc31c37653e5d759b65c25e5ed5/8.Manage%20Azure%20Storage/2.3.2%20generate%20sas%20to%20view%20the%20file%20created.png)
![Alt text](https://github.com/venuGanes/azure/blob/8141524fbfe3fdc31c37653e5d759b65c25e5ed5/8.Manage%20Azure%20Storage/2.3.3%20generate%20sas%20url.png)

## 3) Create and configure secure Azure file storage.

In this task, we will create and configure Azure File shares. we will use Storage Browser to manage the file share.

##### 3.1 Create the file share and upload a file

In this task we'll create a share file with the name "Share1"

![Alt text](https://github.com/venuGanes/azure/blob/b95244287542169a244433e454a431f48edd5608/8.Manage%20Azure%20Storage/3.1%20create%20file%20share.png)
![Alt text](https://github.com/venuGanes/azure/blob/b95244287542169a244433e454a431f48edd5608/8.Manage%20Azure%20Storage/3.1.1%20file%20share%20cereated.png)

##### 3.2 Explore Storage Browser and upload a file

Next, we have to select the Storage Browser (a portal which allows us to view all the storage services under our account) and select the sthe "share1" , add directory and upload a file.

##### 3.3 Restrict network access to the storage account

Lastly, we'll create a virtual network with and name it" vnet1". For the service endpoints will select tbe "Microsoft.Storage". Next we'll add the created "vnet1" under the public network access and also select default subnet and save the changes. We'll delete the machine IP address as the allowed traffic should only come from the virtual network.

![Alt text](https://github.com/venuGanes/azure/blob/b95244287542169a244433e454a431f48edd5608/8.Manage%20Azure%20Storage/3.3.3%20image%20summary%20not%20authorized.png)

