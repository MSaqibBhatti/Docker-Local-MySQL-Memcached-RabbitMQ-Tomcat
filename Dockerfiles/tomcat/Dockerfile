FROM openjdk:11 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/devopshydclub/vprofile-project.git
RUN cd vprofile-project && git checkout dcker


FROM tomcat:9-jre11
LABEL "Project" = "Docker-Local"
LABEL "Author" = "MSaqibBhatti"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE Docker-Local-MySQL-Memcached-RabbitMQ-Tomcat/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["cataline.sh", "run"]

