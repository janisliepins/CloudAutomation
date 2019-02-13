# PetclinicCloudFormation
CloudFormation templates for Petclinic application delivery automation
1. Create Git repository in "CodeCommit" for Petclinic application
2. Configure the application to use MySql as its database
3. Launch NetworkStack.yaml -> Creates VPC network: 2 public and 2 private subnes, 1 Internet Gateway, 2 NAT gateways + 2 elastic IPs, 2 private and 1 public route tables.
4. Launch SecurityStack.yaml -> Creates VPC security groups: 1 for ALBs, 1 for EC2 instances, 1 for databases.
4. Launch Database.yaml -> Creates RDS instance and its replica based on MySql engine in your VPC.
.....
5. Launch PetclinicAppStack.yaml -> Creates shared resources visualized in "Resource architecture overview"
6. Launch PetclinicPipelineStack.yaml -> Creates CodePipeline resources visualized in "Pipeline architecture overview"
7. Change manually db endpoint value in "application-mysql.properties" file -> spring.datasource.url=jdbc:mysql://rds_endpoint/petclinic 

# Test application
Test application used: [here](https://github.com/spring-projects/spring-petclinic)

# Pipeline architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/PetclinicPipelineArchitecture.png)

# Resource architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/PetclinicResourceArchitecture.png)

