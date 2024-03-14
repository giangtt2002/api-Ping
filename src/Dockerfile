FROM amazoncorretto:17-alpine-jdk


# Refer to Maven build -> finalName
ARG JAR_FILE=target/*.jar

RUN apt-get update && apt-get install -y iputils-ping

# cd /opt/app
WORKDIR /opt/app

# cp target/spring-boot-web.jar /opt/app/app.jar
COPY ${JAR_FILE} app.jar

# java -jar /opt/app/app.jar
ENTRYPOINT ["java","-jar","/app.jar"]

CMD bash


