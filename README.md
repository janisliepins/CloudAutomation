# PetclinicCloudFormation
CloudFormation templates for Petclinic application delivery automation
1. Launch PetclinicAppStack.yaml -> Creates shared resources visualized in "Resource architecture overview"
2. Launch PetclinicPipelineStack.yaml -> Creates CodePipeline resources visualized in "Pipeline architecture overview"
3. Change manually db endpoint value in "application-mysql.properties" file -> spring.datasource.url=jdbc:mysql://<endpoint>/petclinic 

# Test application
Test application used: [here](https://github.com/spring-projects/spring-petclinic)

# Pipeline architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/PetclinicPipelineArchitecture.png)

# Resource architecture overview
![ResourceArchitecture](https://github.com/janisliepins/PetclinicCloudFormation/blob/develop/PetclinicResourceArchitecture.png)

