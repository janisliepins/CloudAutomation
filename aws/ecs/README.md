# Continuous delivery with AWS FARGATE & CODEPIPELINE
CloudFormation templates for SpringBoot application and infrastructure automation in AWS.

1. Create Git repository in "CodeCommit" for Petclinic application. Source code [here](https://github.com/spring-projects/spring-petclinic).

2. Configure the application to use MySql as its database (Connection and table creation).

3. Launch RepositoryStack.yaml -> Creates CodeCommit, ECR repositories and S3 bucket.

4. Launch NetworkStack.yaml -> Creates VPC network: 2 public and 2 private subnes, 1 Internet Gateway, 2 NAT gateways + 2 elastic IPs, 2 private and 1 public route tables.

5. Launch IamRoleStack.yaml -> Creates 4 IAM roles for CodePipeline, CodeBuild, ECS Tasks and Services. 

6. Launch DatabaseStack.yaml -> Creates micro 5GB RDS instance and its replica based on MySql engine in your VPC's private subnet + security group.

7. Launch FargateStack.yaml -> Creates ALB and its target, security groups. Creates Fargate cluster, service, task + task definition file and security group.

8. Launch CodePipelineStack.yaml -> Creates CodeBuild project and CodePipeline. 

9. Commit your changes to application or run CodePipeline project and enjoy!


# Stack export value distribution overview
![ResourceArchitecture]()

# NetworkStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/NetworkStack.png)

# NetworkStack + SecurityStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/SecurityStack.png)

# NetworkStack + SecurityStack + DatabaseStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/DatabaseStack.png)

# NetworkStack + SecurityStack + DatabaseStack + ServerStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/ServerStack.png)

# NetworkStack + SecurityStack + DatabaseStack + PipelineStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/PipelineStack.png)

# Example of different stack combinations 
![ResourceArchitecture]()






