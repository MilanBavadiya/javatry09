# Use an official OpenJDK runtime as a parent image
FROM openjdk:17

# Set the working directory in the container
WORKDIR /usr/local/app

# Copy the JAR file from the host to the container
COPY /home/ubuntu/javatry09/Milan/target/myapp.jar /usr/local/app/myapp.jar

# Expose the port the application runs on (change 8080 if your app uses a different port)
EXPOSE 8080

# Run the JAR file
ENTRYPOINT ["java", "-jar", "/usr/local/app/myapp.jar"]
