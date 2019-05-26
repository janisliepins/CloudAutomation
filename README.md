# Nepārtraukta piegāde AWS mākoņvidē ar ECS un CodePipeline

![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/CloudFormationArchitecture/Overview.png)


## Testa aplikācijas sagatavošana

1. Testa aplikācija pieejama [šeit](https://github.com/spring-projects/spring-petclinic) 
2. Pievieno "buildspec.yaml" failu projekta saknes līmenī
3. Pievieno "Dockerfile" projekta saknes līmenī

## Steku izveide

1. Izveido nepieciešamos uzglabāšanas resursus: "StorageStack.yaml" veidni - tiks izveidotas CodeCommit, ECR repozitorijas un S3 krātuve


2. Izveido IAM lomas ar pielāgotiem noteikumu dokumentiem: "SecurityRoleStack.yaml" - tiks izveidotas ECS Service, ECS Task, CodeBuild, CodePipeline lomas


3. Izveido nepieciešamos tīklošanas resursus: "NetworkStack.yaml" - tiks izveidots virtuāls privāts tīkls ar 2 privātiem apakštīkliem, 2 publiskiem apakštīkliem, maršutēšanas tabulām, tīkla ACL, interneta vārteju un 2 NAT vārtejām ar 2 IP adresēm
![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/CloudFormationArchitecture/NetworkStack.png)


4. Izveido EC2 drošības grupas: "SecurityGroupStack.yaml" - tiek izveidotas divas drošības grupas ALB, un VPC tīkla datuplūsmas kontrolei


5. Izveido RDS instanci ar MySQL datubāzi: "DatabaseStack.yaml" - tiks izveidota MySQL datubāze


6. Izveido 2 skaitļošanas stekus DEV un PROD vidēm. CloudWatch, ECS Fargate un EC2 resursus: "ComputeStack.yaml" - tiks izveidots ECS klāsteris, serviss ar Fargate izpildes tipu un konteineri. Papildus tiks izveidota CloudWatch žurnāla grupa un EC2 resursi: aplikāciju slodzes līdzsvarotājs, mērķa grupa un 2 drošības grupas konteineriem un aplikāciju slodzes līdzsvarotājam

![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/CloudFormationArchitecture/ComputeStack.png)


7. Izveido 2 datu konveijerapstrādes stekus: "PipelineStack.yaml" - tiks izveidots CodeBuild un CodePipeline projekts ar 5 piegādes posmiem

![Arhitektūra](https://github.com/janisliepins/CloudAutomation/blob/master/CloudFormationArchitecture/PipelineStack.png)

Augšupielādē projekta kodu CodeCommit repozitorijā!



