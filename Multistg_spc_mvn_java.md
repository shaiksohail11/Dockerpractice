
*** Let us build the app using multistating ***

FROM maven:3.8.6-openjdk-11 as build
RUN git clone https://github.com/spring-projects/spring-petclinic.git && \
 cd /spring-petclinic && \ 
 mvn package

# jar location /spring-petclinic/target/spring-petclinic-2.7.3.jar

FROM openjdk:11
LABEL author="shaik"
LABEL project="multi-staging"
EXPOSE 8080
COPY --from=build /spring-petclinic/target/spring-petclinic-2.7.3.jar /spring-petclinic-2.7.3.jar
CMD ["java", "-jar", "/spring-petclinic-2.7.3.jar"]