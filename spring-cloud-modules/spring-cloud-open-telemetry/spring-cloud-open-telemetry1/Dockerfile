FROM amazoncorretto:21

COPY target/spring-cloud-open-telemetry1-1.0.0-SNAPSHOT.jar spring-cloud-open-telemetry.jar
COPY otel.properties /
COPY opentelemetry-javaagent-2.4.0.jar /

EXPOSE 8090

ENV OTEL_JAVAAGENT_CONFIGURATION_FILE="/otel.properties"

ENTRYPOINT ["java","-javaagent:/opentelemetry-javaagent-2.4.0.jar", "-jar","/spring-cloud-open-telemetry.jar"]
