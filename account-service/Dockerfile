FROM maven:3-jdk-8
MAINTAINER Adam De <developer@noxcuse.pl>

WORKDIR /app

# Add POM and source
ADD pom.xml /app/pom.xml
ADD src /app/src

#Build application
RUN ["mvn", "clean", "package"]
CMD ["sh", "-c", "pwd"]
CMD ["sh", "-c", "ls"]
#Run application
ADD /target/account-service.jar /app/autostop/account-service.jar
CMD ["sh", "-c", "pwd"]
CMD ["sh", "-c", "ls"]
CMD ["java", "-Xmx200m", "-jar", "/app/autostop/account-service.jar"]


# Exposing microservice port
EXPOSE 6000