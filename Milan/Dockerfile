# Use the official Maven image to build the application
FROM maven:3.8.5-openjdk-17 AS build

# Set the working directory
WORKDIR /app

# Copy the Maven project files
COPY pom.xml .
COPY src ./src

# Build the application
RUN mvn clean package

# Use the official Tomcat image to run the application
FROM tomcat:10.1-jdk17

# Copy the WAR file from the build stage to the Tomcat webapps directory
COPY --from=build /app/target/simple-java-web-app.war /usr/local/tomcat/webapps/

# Expose port 8080
EXPOSE 8080

# Start Tomcat
CMD ["catalina.sh", "run"]
