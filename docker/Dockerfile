# Use lightweight Java runtime
FROM eclipse-temurin:17-jre-jammy

# Set working directory
WORKDIR /app

# Copy jar file into container
COPY app/k8s-demo/target/k8s-demo-0.0.1-SNAPSHOT.jar app.jar

# Expose port
EXPOSE 8080

# Run the application
ENTRYPOINT ["java", "-jar", "app.jar"]