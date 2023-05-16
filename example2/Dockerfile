FROM maven:3.9.1-eclipse-temurin-17 AS build
WORKDIR usr/src/springpet
COPY . ./
RUN mvn install
RUN mvn clean package

FROM openjdk:17
WORKDIR /usr/src/springpet
EXPOSE 8080
COPY --from=build /usr/src/springpet/target/spring-petclinic-3.0.0-SNAPSHOT.jar ./spring-petclinic-3.0.0-SNAPSHOT.jar
CMD ["java", "-jar", "spring-petclinic-3.0.0-SNAPSHOT.jar"]
