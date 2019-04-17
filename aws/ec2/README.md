# AWS full infrastructure stack
CloudFormation templates for Spring application and infrastructure delivery automation in AWS.

1. Create Git repository in "CodeCommit" for Petclinic application. Source code [here](https://github.com/spring-projects/spring-petclinic)
2. Configure the application to use MySql as its database (Connection and table creation)
3. Launch NetworkStack.yaml -> Creates VPC network: 2 public and 2 private subnes, 1 Internet Gateway, 2 NAT gateways + 2 elastic IPs, 2 private and 1 public route tables.
4. Launch SecurityStack.yaml -> Creates VPC security groups: 1 for ALBs, 1 for EC2 instances, 1 for databases. 1 Intance IAM role for EC2 access to S3 bucket.
5. Launch DatabaseStack.yaml -> Creates RDS instance and its replica based on MySql engine in your VPC.
6. Launch ServerStack.yaml -> Creates ALB, AutoScaling group with 2 EC2 Instances (HTTPD as webfront -> reverse proxy to localhost Wildfly app server).


# NetworkStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/NetworkStack.png)

# NetworkStack + SecurityStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/SecurityStack.png)

# NetworkStack + SecurityStack + DatabaseStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/DatabaseStack.png)

# NetworkStack + SecurityStack + DatabaseStack + ServerStack architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/aws_cloudformation_architecture/ServerStack.png)

