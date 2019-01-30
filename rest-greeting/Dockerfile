FROM openjdk:8-jdk-alpine
VOLUME /tmp
EXPOSE 9002
COPY target/*.jar app.jar
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/app.jar"]
