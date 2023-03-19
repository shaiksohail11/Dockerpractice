

# Let us build an openmrs-core application

FROM tomcat:8.5.84-jdk8
RUN apt update && apt install git -y && apt install maven -y && git clone https://github.com/openmrs/openmrs-core.git && cd openmrs-core && git checkout 2.6.x && git checkout 053428ace && mvn package
RUN cp -r /usr/local/tomcat/openmrs-core/webapp/target/openmrs.war /usr/local/tomcat/webapps/openmrs.war
EXPOSE 8080


# To check <public-ip:port/openrms>