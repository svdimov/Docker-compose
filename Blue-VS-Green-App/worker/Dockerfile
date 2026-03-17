FROM maven:3.6.3-jdk-8 AS build

WORKDIR /code

COPY pom.xml .
COPY src ./src

RUN mvn clean package -DskipTests

FROM eclipse-temurin:8-jre

WORKDIR /app

COPY --from=build /code/target/worker-jar-with-dependencies.jar /app/worker.jar

CMD ["java", "-jar", "/app/worker.jar"]