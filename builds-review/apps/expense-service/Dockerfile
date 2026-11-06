FROM quay.io/redhattraining/ocpdev-ubi8-openjdk-17-base:latest

COPY pom.xml .
RUN mvn dependency:go-offline

COPY src .
RUN mvn clean package

CMD ["java", "-jar", "target/expense-service-1.0.0-SNAPSHOT-runner.jar"]
