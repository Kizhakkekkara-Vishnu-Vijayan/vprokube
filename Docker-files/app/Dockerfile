FROM maven:3.9.9-eclipse-temurin-21-jammy AS BUILD_IMAGE
RUN git clone -b main https://github.com/Kizhakkekkara-Vishnu-Vijayan/vprokube.git
RUN cd vprokube && mvn install

FROM tomcat:10-jdk21
LABEL "Project"='Vprofile'
LABEL "Author"="Vishnu"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprokube/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
