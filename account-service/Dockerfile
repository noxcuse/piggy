FROM maven:3-jdk-8
MAINTAINER Adam De <developer@noxcuse.pl>

WORKDIR /app

# Add POM and source
ADD pom.xml /app/pom.xml
ADD src /app/src

#Build application
CMD ["mvn", "clean", "package"]

#Run application
ADD /target/account-service.jar /app/autostop/account-service.jar
CMD ["java", "-Xmx200m", "-jar", "/app/autostop/account-service.jar"]

# Exposing microservice port
EXPOSE 6000