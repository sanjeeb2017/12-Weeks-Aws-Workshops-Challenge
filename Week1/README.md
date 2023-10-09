# WEEK -1 : Foundation - AWS Core Services

Welcome to AWS Workshop challenge - Week1. For each week challenge, we will put details on the challenge overview, problem statement / solution approach  and conclusion/learning from the challenge.

**Challenge Overview:**

For each week, we have Basic and Advance challenge. We will attempt both the challenges for the completeness.

**`Basic Modules:`**

In this challenge, we will learn the foundation or imporant services of AWS. However before deep dive into AWS services, we will first understand below fundamental concepts.

1. Overview of Cloud Computing and deployment types.
2. Benifits of Cloud Computing.
3. What is AWS Cloud and its eco system.
4. Fundemnatal /Core services of AWS.

**Problem Statement:**

For any new person who is interested to start the cloud journey, it is very important to know basic details on the cloud computing and different cloud service providers in the current market. In this workshop challenge, the main focus is AWS, so it is very important to understand what is AWS and core services of AWS.

**Solution:**

Let's start the discussion.

**`1.What is Cloud Computing:`**

**Cloud Computing** is on demand delivery of computing services such as compute, storage, databases, networking, software, analytics, and intelligence over the Internet so called cloud.It helped organization to provision the infrastructure in quick time compare to traditional approach where it took months to build the infrastructure. It eliminates the need for enterprises to procure, configure, or manage resources themselves, and they only pay for what they use and zero or less administration on the infrastructure.

There are three types of cloud computing service models.
1. IaaS ( Infrastrure as a Service): It offers compute and storage services.
2. PaaS ( Platform as a Service) : It offers a develop-and-deploy environment to build cloud apps.
3. SaaS ( Software as a Service) : It delivers apps as services.

There are 3 different **cloud computing deployment** models available i.e public cloud, private cloud, and hybrid cloud. 

**`Public Cloud:`**

Public clouds are run by third-party cloud service providers. They offer compute, storage, and network resources over the internet, enabling companies to access shared on-demand resources based on their unique requirements and business goals. The main 3 public cloud providers are AWS, Google, GCP

**`Private Cloud:`**

Private clouds are built, managed, and owned by a single organization and privately hosted in their own data centers, commonly known as “on-premises” or “on-prem.” They provide greater control, security, and management of data while still enabling internal users to benefit from a shared pool of compute, storage, and network resources.

**`Hybrid Cloud:`**

Hybrid clouds combine public and private cloud models, allowing companies to leverage public cloud services and maintain the security and compliance  capabilities commonly found in private cloud architectures.

**`2.Benifits of Cloud Computing`**

1. Flexible and easy to use. User can access the environment any where from the world, just need the internet access.
2. Pay as you go model. Pay what you have used. It is very cost effective. User can always spin up server with couple of clicks and start the developement of business usecase and start seeing the values quickly.
3. Secure, cloud service providers are align with most of the compliance requirements, by saying that security is a shared responsibilty. 

cloud has many advantage but we just listed some of them above.

**`3.What is AWS cloud:`**

AWS stands for Amazon Web Service. AWS is the top public cloud service provider.Amazon Web Services (AWS) is the world’s most comprehensive and broadly adopted cloud, offering over 200 fully featured services from data centers globally. Millions of customers including the fastest-growing startups, largest enterprises, and leading government agencies are using AWS to lower costs, become more agile, and innovate faster. The details on AWS can be found - https://aws.amazon.com/?nc2=h_lg

Before we will understand the core services of AWS, couple of pre-requisites we have to complete.

_**`Create an AWS account`**_

 To explore AWS world, it is very important to create an AWS account. We are not going to cover how to create an AWS account as the process is very simple. To get the step by step proces, please have a look on the youtube video - https://www.youtube.com/watch?v=XhW17g73fvY.

_**`Create an IAM user`**_

The IAM user (IAM stands for Identitya and Access Management)is the human user or workload who uses the IAM user to interact with services of AWS. A user in AWS consists of a name and credentials. When a user is created its account for the first time with details, the user is called as a root user. Once the root user is created, it is recommended to create another IAM User with administrative privilages. Root users are not used for day to day activities.

Follow the below steps, to create an IAM user with administrative privilage.
1. Go to AWS Management console - Link - https://aws.amazon.com/console/ and login with your root credential. Search IAM in the search console. Click on IAM Service.
2. To create an IAM user, click on Users in the left panel.
3. Click on the Create User
4. Give the username, In our case, we provided the name - aws-workshop-challenge. We need to login AWS management console using this user, so select the option "Provide user access to the AWS Management Console - optional", select the option (I want to create an IAM user)
5. For simplicity, select custom password and give a custom password and unchecked the option - Users must create a new password at next sign-in - Recommended. If you want to change your password upon your first login, you can select this option. Click Next.
6. You can create a group so that you can orginze the users and assign the permission at group level for better user and access management. To create a group, click create group.
7. Give the user group name, in our case we provided the group name as aws-admin-group. Select the AdministratorAccess and click create user group.
8. Select the newly created group so that user will added to that group and inherit the adminsirator privilage. Click Next
9. Review the details and click the create user to create an IAM user with administrator privilage.
10. Download the credentail .csv file ( Do Not Share your credentials)
11. To ensure, the new user is able to login AWS management console, logout the current session and login with AWS management console with new user credential. The credental details also available in the .csv file. Open the .csv file to get the sign in URL and provide the details and validate your login.

Well Done!! We did our first hands on AWS cloud, create an adminstrator IAM user. As per the best pratice, we should create another IAM user and provide the least permission to do the work. However for completing the workshop challenges, we will use this new user id. In real production implementation, the least privilage principle is followed to ensure right user have right access.

All the above steps are presented in the below screenshots for better understanding.

<img width="557" alt="image" src="https://github.com/sanjeeb2017/12-Weeks-Aws-Workshops-Challenge/assets/24868114/9d6ad5b1-a60a-40dc-9dec-25a74e6c6e19">

<img width="500" alt="image" src="https://github.com/sanjeeb2017/12-Weeks-Aws-Workshops-Challenge/assets/24868114/31d54289-6487-47c9-bbfd-224bb4f583fc">

<img width="497" alt="image" src="https://github.com/sanjeeb2017/12-Weeks-Aws-Workshops-Challenge/assets/24868114/b56c8ee7-92e7-4dc7-b4ce-dd86299c5ccd">

<img width="349" alt="image" src="https://github.com/sanjeeb2017/12-Weeks-Aws-Workshops-Challenge/assets/24868114/81b78460-245d-4f5c-b58e-0e286f06e41f">

<img width="500" alt="image" src="https://github.com/sanjeeb2017/12-Weeks-Aws-Workshops-Challenge/assets/24868114/9e2bc96d-3bf8-4936-aa28-fd098fba14aa">

<img width="508" alt="image" src="https://github.com/sanjeeb2017/12-Weeks-Aws-Workshops-Challenge/assets/24868114/eb9d48fd-f901-46a2-bb18-19401c95863f">

<img width="622" alt="image" src="https://github.com/sanjeeb2017/12-Weeks-Aws-Workshops-Challenge/assets/24868114/141cef60-eeaa-4d91-80fc-a85301f9fb20">


**`4.Core Services of AWS:`**




