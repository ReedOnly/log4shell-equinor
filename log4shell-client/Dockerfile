FROM maven:3.2.3-jdk-8u40 as build

WORKDIR /app
COPY . .
RUN mvn clean install

CMD mvn exec:java && tail -f /dev/null
