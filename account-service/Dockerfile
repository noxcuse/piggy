FROM maven:3-jdk-8
MAINTAINER Adam De <developer@noxcuse.pl>

WORKDIR /app

# Add POM and source
ADD pom.xml /app/pom.xml
ADD src /app/src

#BuildAppX
RUN ["mvn", "clean", "package"]

ADD ./target/account-service.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/account-service.jar"]

EXPOSE 6000