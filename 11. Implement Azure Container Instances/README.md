# Lab scenario

In this lab, you learn about Azure web apps. You learn to configure a web app to display a Hello World application in an external GitHub repository. 
You learn to create a staging slot and swap with the production slot. You also learn about autoscaling to accommodate demand changes.

This lab requires an Azure subscription. Your subscription type may affect the availability of features in this lab. You may change the region, but the steps are written using East US.

Your organization is interested in Azure Web apps for hosting your company websites. The websites are currently hosted in an on-premises data center. The websites are running on Windows servers using the PHP runtime stack. 
The hardware is nearing end-of-life and will soon need to be replaced. Your organization wants to avoid new hardware costs by using Azure to host the websites.

# Architecture Diagram
![Alt text]()

# Objective

- [x]Task 1: Create and configure an Azure web app.
- [x]Task 2: Create and configure a deployment slot.
- [x]Task 3: Configure web app deployment settings.
- [x]Task 4: Swap deployment slots.
- [x]Task 5: Configure and test autoscaling of the Azure web app.
- 
## 1) Create and configure an Azure web app.
 
In this task, you create an Azure web app. Azure App Services is a Platform As a Service (PAAS) solution for web, mobile, and other web-based applications. 
Azure web apps is part Azure App Services hosting most runtime environments, such as PHP, Java, and .NET. The app service plan that you select determines the web app compute, storage, and features.

![Alt text]()


## 2) Create and configure a deployment slot.

In this task, you will create a staging deployment slot. Deployment slots enable you to perform testing prior to making your app available to the public (or your end users). 
After you have performed testing, you can swap the slot from development or staging to production. Many organizations use slots to perform pre-production testing. 
Additionally, many organizations run multiple slots for every application (for example, development, QA, test, and production).

![Alt text]()

## 3) Configure web app deployment settings

In this task, you will configure Web App deployment settings. Deployment settings allow for continuous deployment. This ensures that the app service has the latest version of the application.

## 4) Swap deployment slots.
In this task, you will swap the staging slot with the production slot. Swapping a slot allows you to use the code that you have tested in your staging slot, and move it to production. 
The Azure portal will also prompt you if you need to move other application settings that you have customized for the slot. 
Swapping slots is a common task for application teams and application support teams, especially those deploying routine app updates and bug fixes.

## 5) Configure and test autoscaling of the Azure web app.
In this task, you will configure autoscaling of Azure Web App. Autoscaling enables you to maintain optimal performance for your web app when traffic to the web app increases.
To determine when the app should scale you can monitor metrics like CPU usage, memory, or bandwidth.
