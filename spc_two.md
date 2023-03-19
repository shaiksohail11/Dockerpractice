*** Now let us create  a docker file with slim image deom docker hub(AMAZON CORRETTO)..***

*** Here we are using a new command called 'ADD' Which will copy the files into images i.e (Source to destination) ***


FROM amazoncorretto:11
ADD https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/spring-petclinic-2.4.2.jar /spring-petclinic-2.4.2.jar
EXPOSE 8080
CMD ["java", "-jar", "/spring-petclinic-2.4.2.jar"]