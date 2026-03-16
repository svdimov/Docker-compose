FROM openjdk:11.0.1-jre-slim

LABEL maintainer="Stefan"

ARG JAR_FILE=target/*.jar

COPY ${JAR_FILE} app.jar

EXPOSE 8080

ENTRYPOINT [ "java", "-jar", "app.jar" ]
