FROM maven:3-jdk-8-slim as build
WORKDIR /app

COPY . .
RUN mvn clean install

FROM tomcat:8.0.36-jre8
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=build app/target/log4shell-1.0-SNAPSHOT.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080

CMD ["catalina.sh", "run"]
