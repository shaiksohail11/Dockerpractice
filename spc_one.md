## Writing a docker file, to run a java application called #spring-pet-clinic ##


FROM ubuntu:22.04
RUN sudo apt update
RUN Sudo apt install openjdk-11-jdk wget -y
RUN wget https://springpetcli.s3.ap-southeast-2.amazonaws.com/spring-petclinic-3.0.0-SNAPSHOT.jar
EXPOSE 8080
CMD ["java", "-jar", "/spring-petclinic-2.4.2.jar"]
