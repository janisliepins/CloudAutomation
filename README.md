# PetclinicCloudFormation
CloudFormation templates for Petclinic application delivery automation
1. Create Git repository in "CodeCommit" for Petclinic application. Source code [here](https://github.com/spring-projects/spring-petclinic)
2. Configure the application to use MySql as its database
3. Launch PetclinicAppStack.yaml -> Creates shared resources visualized in "Resource architecture overview"
4. Launch PetclinicPipelineStack.yaml -> Creates CodePipeline resources visualized in "Pipeline architecture overview"
5. Change manually db endpoint value in "application-mysql.properties" file -> spring.datasource.url=jdbc:mysql://rds_endpoint/petclinic 


# Pipeline architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/PetclinicPipelineArchitecture.png)


# Resource architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/PetclinicResourceArchitecture.png)

