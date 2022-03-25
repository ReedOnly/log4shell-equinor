FROM tomcat:8.0.36-jre8

# RUN apt update
# RUN apt install -y netcat
RUN rm -rf /usr/local/tomcat/webapps/*
ADD target/log4shell-1.0-SNAPSHOT.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
EXPOSE 22
CMD ["catalina.sh", "run"]
