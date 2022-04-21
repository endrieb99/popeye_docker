FROM maven:3.5-jdk-8-alpine as builder

MAINTAINER Endri Bida

COPY ./pom.xml ./pom.xml

COPY ./src ./src

RUN mvn dependency:resolve

RUN mvn package

FROM openjdk:8-jre-alpine

WORKDIR /code

COPY --from=builder code/target/worker-jar-with-dependencies.jar /code

CMD ["java -jar worker-jar-with-dependencies.jar"]