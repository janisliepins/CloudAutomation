# Docker pamata imidža nosaukums, kuru lejupielādēt no DockerHub publiskā reģistra
FROM openjdk:8-jdk-alpine
# kopēt .jar tipa failus no target direktorijas uz Docker imidža noklusēto darba direktoriju
COPY target/*.jar petclinic.jar
# komandas, kas tiks izpildītas vispirms, kad tiek izpildīts Docker imidžs kā konteiners
ENTRYPOINT ["java","-jar","petclinic.jar","--spring.profiles.active=mysql"]
