# Stage 1: Build the application
FROM openjdk:11 AS BUILD_IMAGE
LABEL "Project"="Vprofile"
LABEL "Author"="Chidi"
RUN apt update && apt install -y maven
RUN git clone https://github.com/chiddy158/vprofile-project.git
RUN cd vprofile-project && git checkout docker && mvn install

# Stage 2: Create the final image
FROM tomcat:9-jre11
COPY --from=BUILD_IMAGE /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
