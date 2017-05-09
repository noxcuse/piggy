FROM maven:3-jdk-8
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>

#Build
RUN ["mcn", "clean", "package"]

ADD ./target/account-service.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/account-service.jar"]

EXPOSE 6000