# How to Deploy a MERN Stack Application to Production on Code Capsules

Deploy a MERN (MongoDB, Express, React, Node) stack application using a backend and data capsule for the full stack without a frontend capsule. 

## Getting Started

This guide is a walkthrough on how to deploy a MERN stack application that accepts a name as input and displays a personalized message for the user. The example application we will use can be found on [Code Capsules' GitHub](https://github.com/codecapsules-io/mern-stack) account.

Fork the project in the above mentioned repository to your own GitHub repository and link it with your Code Capsules account. 

## Setting Up the Capsules

Create a Space which will house the backend and data capsules needed to successfully deploy the application. Once the Space is there, create the two capsules as shown below.

First the data capsule.

![MongoDB Database Cluster](../assets/reference/mongodb-database-cluster.png)

Followed by the backend capsule.  

![Create Backend Capsule](../assets/deployment/python/creating-backend-capsule.gif)

Select the repository you forked earlier and in the "Run Command" field enter `node index.js` to let the capsule know how to run your application.

## Binding the Capsules

After successfully building the capsules the next step is to bind them together. Navigate to the backend capsule you just created and open the "Configure" tab. Scroll to the bottom and click on the "Bind" option in the bottm left to allow the capsule to use the MongoDB in the data capsule. 

![Bind MERN Capsules](../assets/deployment/mern/bind-mern-capsules.png)

## View Application

The application will be ready for use after binding the two capsules together. To view it, click on the "Live Website" link at the top of your backend capsule page.

![Live Website Link](../assets/deployment/mern/live-website-link.png)

## View Application Logs

You can also view your application's logs by navigating to the "Logs" tab on your backend capsule page.

![Application Logs](../assets/deployment/mern/application-logs.png)