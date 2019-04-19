# Continuous delivery with AWS FARGATE & CODEPIPELINE
CloudFormation templates for SpringBoot application and infrastructure automation in AWS

1. Download test application source code [here](https://github.com/spring-projects/spring-petclinic) or use already prepared version in application folder

2. If the original one is used, you leave only scr/ folder and pom.xml file. Add Dockerfile and buildspec.yaml files at the root level in source code

3. Launch StorageStack.yaml -> Creates CodeCommit, ECR repositories and S3 bucket
![ResourceArchitecture](https://github.com/janisliepins/CloudAutomation/blob/master/aws/ecs/CloudFormationArchitecture/storage_stack.png)

4. Upload application source code to CodeCommit repository

5. Launch IamRoleStack.yaml -> Creates 4 IAM roles for CodePipeline, CodeBuild, ECS Tasks and Services with needed policies 
![ResourceArchitecture](https://github.com/janisliepins/CloudAutomation/blob/master/aws/ecs/CloudFormationArchitecture/iamrole_stack.png)

6. Launch NetworkStack.yaml -> Creates VPC network: 2 public and 2 private subnes, 1 Internet Gateway, 2 NAT gateways + 2 elastic IPs, 2 private and 1 public route tables.

6. Launch DatabaseStack.yaml -> Creates micro 5GB RDS instance and its replica based on MySql engine in your VPC's private subnet + security group.

7. Launch FargateStack.yaml -> Creates ALB and its target, security groups. Creates Fargate cluster, service, task + task definition file and security group.

8. Launch CodePipelineStack.yaml -> Creates CodeBuild project and CodePipeline. 

9. Commit your changes to application or run CodePipeline project and enjoy!








