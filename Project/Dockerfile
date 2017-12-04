FROM openjdk:8-jdk-alpine
ADD target/apptest.jar apptest.jar
ENTRYPOINT exec java -jar apptest.jar
EXPOSE 8080