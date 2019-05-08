# Nepārtraukta piegāde AWS mākoņvidē ar ECS un CodePipeline

## Testa aplikācijas sagatavošana

1. Jau sagatavota testa aplikācija pieejama "TestApplication" mapē. Oriģināls pieejams [šeit](https://github.com/spring-projects/spring-petclinic) 

## Steku izveide

1. Izveido nepieciešamos uzglabāšanas resursus: "StorageStack.yaml" veidni - tiks izveidotas CodeCommit, ECR repozitorijas un S3 krātuve
![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/aws/ecs/CloudFormationArchitecture/storage_stack.png)


2. Izveido IAM lomas ar pielāgotiem noteikumu dokumentiem: "IamRoleStack.yaml" - tiks izveidotas ECS Service, ECS Task, CodeBuild, CodePipeline lomas
![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/aws/ecs/CloudFormationArchitecture/iamrole_stack.png)


3. Izveido nepieciešamos tīklošanas resursus: "NetworkStack.yaml" - tiks izveidots virtuāls privāts tīkls ar 2 privātiem apakštīkliem, 2 publiskiem apakštīkliem, maršutēšanas tabulām, tīkla ACL, interneta vārteju un 2 NAT vārtejām ar 2 IP adresēm
![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/aws/ecs/CloudFormationArchitecture/network_stack.png)


4. Izveido RDS instanci ar MySQL datubāzi: "IamRoleStack.yaml" 


5. Izveido CloudWatch, ECS Fargate un EC2 resursus: "FargateStack.yaml" - tiks izveidots ECS klāsteris, serviss ar Fargate izpildes tipu un konteineri. Papildus tiks izveidota CloudWatch žurnāla grupa un EC2 resursi: aplikāciju slodzes līdzsvarotājs, mērķa grupa un 2 drošības grupas konteineriem un aplikāciju slodzes līdzsvarotājam






