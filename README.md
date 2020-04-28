
# **AWS**  

**-   What is Clund ?**    
**-   What is AWS ?**       
**-   Different Domains in AWS**        
**-   AWS Services**    
**-   AWS Pricing Options**     
**-   Migrating your application to AWS Infrastructure**        
**-   Architecting the Use Case**

#

1.  **Cloud computing** : is the use of remote servers to store, manage and process data. So, you do three things, you store, you manage, and you process data.
	-   You are storing a file, say on a file system on the Cloud.
	-   You are managing a data using database there on the Cloud.
	-   You process your data, using computing power on the cloud to process your data.
     
2. **Amazon Web Services (AWS)** is a secure cloud services platform,  offering compute power, database storage, content delivery and other functionality to help businesses scale and grow.  

3. **Different Domains in AWS**
	- **Compute domain** : There is a service called **EC2**. EC2 is an Elastic Compute Cloud, is just like a raw server. you can configure this server to be anything. You can use it to host a website, use it as work at your enviroment, its a clean state, its just linke a new PC that you buy, you can install a fresh operating system on your PC, and then you can configure it to be anything, and solve any software you want, and then it can serve you as you require. And that is what EC2 dose as well. So this is the Compute Domain.
	- **Migrating domain** : is when you want to transfer your data to the AWS infrastructure or you want to transfer your data back from AWS infrastructure. Next up we have the **Migration Service** is used to transfer data to and from the AWS Infrastructure.  example you have petabytes scale of data in your data center and you want to send it to AWS Infrastructure, you will be using services in migration.
	-  **Security & Identity, Compliance** : In security and identity compliance, you have services like IAM, which is uesd to authenticate users and define suer rights to them. Suppose you are running a company and you have a root AWS account, you want other employees to work on AWS account as well, but you want then to have restricted access, suppose you want user 1 to maybe just launch instances and user 2 can only edit instances, but not launch instances, maybe user 3 can only review the instances not launch or edit these instances, all of these granular permissions can be given to your users using IAM and that is was what Security and Identity Compliance domain is all about.
	- **Storage Domain** :  would include services link **S3** which is **Simple Storage Service**. its a file system, it's an object-based file system, in which you can store your files and access then as and when required. People usually get confused between Storage domain and Database domain, because basically they are storing data, so why 2 different domains. 
	- **Storage**  would include service like S3, so its a file system. what is the difference between a file system and database. So, a database cannot include your executable files, suppose you have an image file, that image file would not be stored in a database , its better to store that image file in a file system and hence, access that image file using a path, which can be stored in the database, this is the basically the difference between a file system and a database.
	- **Networking and Content Delivery** : includes services like **Route 53**. Route 53 is a domain name system which basically redirects your traffic from the URL that you purchase, say domain selling website like GoDaddy and redirects it to your instances or your servers which are hosting your web application. why do we do this ? Because you connot remember the IP addresses, you need something solid, you need something simple and that is what domain name system is all about. it translates the simple into the IP address and redirects your traffic to that IP address. So, this is about Route 53.
	- **Messaging domain** : is all about services like, say suppose simple email servers. it is used to send emails in bulk to your customers base, if you have as application where you have to notify your customers about new update. So, rather than sending emails to each and every customer, with the click of a button, you can send it using **SES**, and you can also handle the replies that customers gives. So, all of that can be managed using SES which is **Simple Email Service**, which comes under the Messaging domain.
	- **Database domain** : would include services link RDS, a **relational data service** basically manages some database for you. Its not a database in itself, but its a managing service, which manages databases for you, so it can manage databases like MySQL, PostgreSQL, they can automatically update the DB engines or they can automatically commit to your changes. All of that is managed using a management service in Amazon, which is RDS, which comes under the database domain.
	- **Management Toos** : are basically tools using which you can manage your AWS resources. In this domain, you have services like **Cloud Watch**, which is an all-in-one cloud monitoring tool. You can use these tools and monitor all the AWS Resources that you are running in your AWS infrastructure.

4. **AWS Services**
	- **AWS Compute Services** : The first service is **EC2**. EC2 is the most important service in the whole of the **Compute Domain**. why do I say it's the most important service ?  Because EC2 is the base and the other services which are, **Lambda** and **Elastic Beanstalk** are just advanced versions of EC2, is just like a raw server, you can configure this raw server or EC2 to be anything. You can configure it to be a web server, it can be configured to become a work at your environment or something else, and this web server can be resized according to you needs. The instances or the server that you have launched, they cana be replicated, as in, you can launch multiple servers of the same configuration or you can also increase the configuration as well, So this is the kind of resizeability that you get with EC2 and this is what EC2 is all about. 
	- **AWS Lambda** : is an avancesd version of EC2, so its based on EC2, but difference between EC2 and Lambda is Lambda cannot be used to host your application. Lambda can be use only to execute your background tasks. what are your background tasks ? suppose you have an application, your application is all about images, so when you upload an image, the image is compressed and it is stored on a file system. So, your image first will be uploaded to the file system, when the image is uploaded, that is performed by a application . Now, the tasks which have to be done in the background like compression, maybe you have some more tasks like applying filters and everying, these tasks are background tasks and these tasks can be executed using AWS Lambda. Now, how does **AWS Lambda functions** is like this: **AWS reponds to events**. So, there are triggers that you set up in AWS Lambda and in reponse to these triggers AWS executes the code. In this case in our expamples that you took that we are uploading a file, or uploading an image, the moment that image gets uploaded to say, suppose S3 which is the file system for AWS, a trigger is generated and that trigger is being listened by AWS Lambda, when that event is listened by AWS Lambda, it responds to that event using the code that you provide, it executes that code and then sits again and waits for another event to happen. Now that code would include your code for compression, applying filters etc. and that is how AWS Lambda functions.
	- **Elastic Beanstalk** : Elastic Beanstalk is again an advanced version of EC2. But with this the difference between Lambda, and EC2 and Elastic Beanstalk is, that first of all Elastic Beanstalk is used to host an application. So if you compare it with AWS Lambda, this is the difference. Elastic Beanstalk is used to host an application, Lambda is not used to host an application. Now, let's talk about **EC2** and **Elastic Beanstalk**. So, Elastic Beanstalk is an automated form of your EC2, How ? with Elastic Beanstalk, you don't have to configure in all the details, or you don't have to set up your environment. Suppose you have PHP website that you want to host on EC2. Now, for your PHP website to be hosted, you first have to create a PHP environment in your EC2. But with Elastic Beanslalk, you don't have to do that, you just have to select what kind of environment do you want, and AWS will install all the configuration files required and will give you the environment on which you just have to upload your code and your application or your website will be deployed. So this is how simple, Elastic Beanstalk is. You create your environment, and then you upload your code, that is it. Nothing else is required. **when would you use EC2 and when would you use Elastic Beanstalk ?** So, Elastic Beanstalk has a limited numbers of environments. So, if you have an environment or an application, which has to be hosted and the environment is listed in Elastic Beanstalk, you should go ahead with Elastic Beanstalk. But, say, suppose your evironment is not there in Elastic Beanstalk, maybe, Elastic Beanstalk, maybe, Elastic Beanstalk is not ready to host your environment yet, may be your used case is not about hosting an application, in that case you will be using EC2.
	- **Elastic Load Balancer** : is basically is used to distribute your work load among a number of instances.  Now, the traffic which will be coming on to these instances has to be distributed equally amoung these 5 or 6 instances, and this is what, Elastic Load Balancer does. Now, why is this important, say suppose you have 4 or 5 servers running and all the traffic is directed to your first instance, so, it doesn't make sense, because all your other 4 servers are idle. You have the capactiy with you, but you have not installed the protocol using which the traffic can be distributed to these 5 instances, and that protocol is Elastic Load Balancer. So, Elastic Load Balancer distributes the work load equally among the instances, so, that the work is done efficiently and also the work is consistent as in.
	- **AutoScaling** :  is a service which is used to scale up and down automatically, without your manual intervention. Now, how do you do that ? you set up matrix. Now, say suppose you have a website running and that website is running on 5 servers, and you configure a matrix that whenver combined CPU useage goes beyond 70%, it will launch a new server and then, focus guys, then the traffic will be distributed among the 6 instances. This work is done by Elastic Load Balancer and that is why AutoScaling and Elastic Load Balancer go hand-in-hand. They have to be used together. So if you are using AutoScanling, you have to use Load Balancer as well. And like said you can scale up using that matrix and you can also set a matrix for scaling down, say suppose your combined CPU usage gose below 50% or gose below 10%, so, you can configure your  AutoScanling to decommission a server in that case and hence you can scale down from the number of instances that you are running and again, your work load will now be distributed to, if you have 5 servers before, it will now be distributed to 4 servers, which again incorporates Elastic Load Balancer. like said AutoScanling and Elastic Load Balancer have to be used together.
