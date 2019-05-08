# Nepārtraukta piegāde AWS mākoņvidē ar ECS un CodePipeline.

## Testa aplikācijas sagatavošana

1. Jau sagatavota testa aplikācija pieejama "TestApplication" mapē. Oriģināls pieejams [šeit](https://github.com/spring-projects/spring-petclinic) 

## Steku izveide

1. Izveido nepieciešamos uzglabāšanas resursus: "StorageStack.yaml" veidni - tiks izveidotas CodeCommit, ECR repozitorijas un S3 krātuve
![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/aws/ecs/CloudFormationArchitecture/storage_stack.png)


2. Izveido IAM lomas ar pielāgotiem noteikumu dokumentiem: "IamRoleStack.yaml" - tiks izveidotas ECS Service, ECS Task, CodeBuild, CodePipeline lomas
![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/aws/ecs/CloudFormationArchitecture/iamrole_stack.png)


3. Izveido nepieciešamos tīklošanas resursus: "NetworkStack.yaml" - tiks izveidots virtuāls privāts tīkls ar 2 privātiem apakštīkliem, 2 publiskiem apakštīkliem, maršutēšanas tabulas, interneta vārteja un 2 NAT vārtejas


4. Izveido RDS instanci ar MySQL datubāzi: "IamRoleStack.yaml" 








