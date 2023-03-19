
*** Now let us run a game of life app, with tomcat 8 or 9 ***


FROM tomcat:8-jdk8
EXPOSE 8080
ADD https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/gameoflife.war /usr/local/tomcat/webapps/gameoflife.war
CMD ["catalina.sh", "run"]


*** To build the image ==> docker image build -t gol:0.1 .  ***
