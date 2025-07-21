FROM maven:3.9.10-eclipse-temurin-17-alpine AS build

WORKDIR /voting

COPY ./voting /voting

#RUN mvn dependency:go-offline

RUN mvn clean package -DskipTests

FROM openjdk:19-jdk-alpine3.16

WORKDIR /voting

COPY --from=build /voting/target/voting-0.0.1-SNAPSHOT.jar /voting

EXPOSE 8080

CMD ["java", "-jar", "voting-0.0.1-SNAPSHOT.jar"]

