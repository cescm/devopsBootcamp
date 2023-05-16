# devopsBootcamp
For example1 and 2, you need to first, clone the repository https://github.com/spring-projects/spring-petclinic and inside the cloned repository, put the provided file Dockerfile
Excercise 1: use a maven container to build a spring application
  docker run –it --name maven_builder –v “$(pwd):/usr/src/building” –w /usr/src/building maven:3.9.1-eclipse-temurin-17 mvn clean install

Excercise 2: use a Dockerfile to create an image running a jar application built with maven
  docker build –t spring:test .
  docker run –it –-name springpet –p 8082:8080 spring:test

Exercise 3: use a dockerfile to create an image running a war application deployed inside a tomcat
  docker build –t sample:test .
  docker run –it –-name sample –p 8081:8080 sample:test

Exercise 4: use a docker compose to create a stack
  docker-compose –f bookstack.yml up -d

# devopsBootcamp
For example1 and 2, you need to first, clone the repository https://github.com/spring-projects/spring-petclinic and inside the cloned repository, put the provided file Dockerfile
Excercise 1: use a maven container to build a spring application
  

    docker run –it --name maven_builder –v “$(pwd):/usr/src/building” –w /usr/src/building maven:3.9.1-eclipse-temurin-17 mvn clean install

Excercise 2: use a Dockerfile to create an image running a jar application built with maven

     docker build –t spring:test .
     docker run –it –-name springpet –p 8082:8080 spring:test

Exercise 3: use a dockerfile to create an image running a war application deployed inside a tomcat

      docker build –t sample:test .
      docker run –it –-name sample –p 8081:8080 sample:test

Exercise 4: use a docker compose to create a stack

      docker-compose –f jenkins.yml up -d
