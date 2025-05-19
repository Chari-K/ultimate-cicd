# Use a maintained and secure Java 17 Alpine base
FROM eclipse-temurin:17-jre-alpine

# Optional: non-root user for better security
RUN addgroup -S app && adduser -S app -G app
USER app

# Path to the compiled JAR from Maven
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

# Copy the JAR file into the container
COPY ${artifact} app.jar

# Start the Spring Boot app
ENTRYPOINT ["java","-jar","app.jar"]
