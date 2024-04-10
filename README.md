Deploying AWS Infrastructure with CloudFormation and CodePipeline

## Introduction
In this project, we'll explore how to deploy AWS infrastructure using AWS CloudFormation along with AWS CodePipeline for continuous integration and continuous delivery (CI/CD). We'll cover creating S3 buckets, configuring them as static websites, setting up network layers with VPCs and subnets, deploying EC2 instances, and duplicating resources across AWS Regions. This tutorial assumes basic familiarity with AWS services.


## Task 1: Creating an S3 Bucket with CloudFormation
1. Create an AWS CloudFormation template (`S3.yaml`) defining an S3 bucket resource.
2. Use AWS CLI to deploy the CloudFormation stack with the template.

![Task 1-1](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/050e7509-651f-47bc-a1c8-6c866e28afce)
![Task 1-2](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/b569765f-e9e6-4314-aaa2-1bea56e1dcee)
![Task 1-3](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/bc62ed21-0a89-4117-b499-72a345998244)



## Task 2: Configuring the Bucket as a Website
1. Update the CloudFormation template to configure the S3 bucket as a static website.
2. Use AWS CLI to update the CloudFormation stack with the modified template.

![Task 2-1](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/077a92e8-fda7-4116-a01b-65ebc0633925)
![Task 2-2](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/6aba72a1-f00c-4b7b-8e46-71d62df97c16)
![Task 2-3](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/1831c6e8-54d2-4c7f-b7c2-69183564cc35)



## Task 3: Cloning a CodeCommit Repository
1. Clone a CodeCommit repository containing CloudFormation templates.
2. Set up version control for CloudFormation templates using CodeCommit.

![Task 3-1](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/00217290-137e-4d38-b6a3-b984233bfc5e)



## Task 4: Creating a Network Layer with CloudFormation and CodePipeline
1. Create a CloudFormation template (`cafe-network.yaml`) to define VPC, subnets, and other network resources.
2. Push the template to the CodeCommit repository to trigger the pipeline.
3. Observe the pipeline creating the CloudFormation stack automatically.

![Task 4-1](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/c31838da-e878-4193-95b6-d2b7ac6c7216)
![Task 4-2](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/eb755327-95fe-4c35-81fa-4d2d1ae48ad8)
![Task 4-3](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/c21ae348-8b1c-481b-9225-6586c5318b87)



## Task 5: Updating the Network Stack
1. Update the network stack to export essential information about created resources.
2. Use AWS CLI to update the CloudFormation stack.

![Task 5-1](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/eb031584-1df4-4215-862a-cd8aca385b6a)
![Task 5-2](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/0e8c48b6-63c1-4f76-852b-5336bda1c8ff)



## Task 6: Defining an Application Stack
1. Create a CloudFormation template (`cafe-app.yaml`) to deploy a dynamic website (e.g., EC2 instance).
2. Push the template to the CodeCommit repository to trigger the pipeline.
3. Observe the pipeline creating or updating the application stack.

![Task 6-1](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/d093a13e-b24c-4dc4-960f-8daddaeb6144)
![Task 6-2](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/b7897cb5-3f58-43d3-b8ca-97c0960e3d43)
![Task 6-3](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/0a07abc4-f072-40e7-ac70-2c4323c2930c)
![Task 6-4](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/b5f55f3d-2271-4f52-9a33-7443560f1e92)
![Task 6-5](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/9792e12e-f42f-49a3-b353-c0a4d6a8bc24)
![Task 6-6](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/29cdd572-55e9-457d-ac38-8c5e7b90a231)



## Task 7: Duplicating Resources to Another Region
1. Use AWS CLI to duplicate network resources (VPC, subnets, etc.) in another AWS Region.
2. Use AWS CloudFormation console to create the application stack in the second Region.

![Task 7-1](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/32fc9240-f424-4da9-9b38-c91715029d56)
![Task 7-2](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/6b34431a-d572-4a05-9b6b-233089385e4f)
![Task 7-3](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/c446a362-b3d4-427e-b7ef-b37595efedea)
![Task 7-4](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/6933cac1-5b78-401d-b67b-cfb1e79c5dee)
![Task 7-5](https://github.com/paonaragdao/Creating-and-implementing-Cloud-Infrastructure-as-Code-using-Cloud-Platform-Templates./assets/48607496/c471ba6e-9bb9-4b94-8d87-3c086f200c75)


## Conclusion
In this project, we've learned how to deploy AWS infrastructure using CloudFormation and automate the process with CodePipeline. We've covered creating S3 buckets, setting up network layers, deploying applications, and duplicating resources across AWS Regions. This approach enhances scalability, reliability, and consistency in managing AWS infrastructure.
