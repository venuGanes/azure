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

![Alt text]
(https://github.com/venuGanes/azure/blob/af339442aa44344b1a97e8c26732fa8653b7e245/8.Manage%20Azure%20Storage/2.1%20task%202%20%20cont%20img%201st.png)

## 2) Create and configure secure blob storage.

In this task, we will create a blob container and upload an image. Blob containers are directory-like structures that store unstructured data.

##### 2.1 Create a blob container and a time-based retention policy

Here, we'll add a container named data 

![Alt text](https://github.com/venuGanes/azure/blob/af339442aa44344b1a97e8c26732fa8653b7e245/8.Manage%20Azure%20Storage/2.1%20task%202%20%20cont%20img.png)
![Alt text]()

##### 2.2 Manage blob uploads

![Alt text]()
![Alt text]()
##### 2.3 Configure limited access to the blob storage


![Alt text]()
## 3) Create and configure secure Azure file storage.

In this task, we will create and configure Azure File shares. we will use Storage Browser to manage the file share.

![Alt text]()

##### 3.1 Create the file share and upload a file
![Alt text]()
##### 3.2 Explore Storage Browser and upload a file

![Alt text]()
##### 3.3 Restrict network access to the storage account
![Alt text]()
