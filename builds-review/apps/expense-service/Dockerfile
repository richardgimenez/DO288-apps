FROM registry.redhat.io/ubi8/openjdk-17:1.23-6.1793585665

COPY pom.xml .
RUN mvn dependency:go-offline

COPY src .
RUN mvn clean package

CMD ["java", "-jar", "target/expense-service-1.0.0-SNAPSHOT-runner.jar"]
