## Relevant Articles
- [OpenTelemetry Setup in Spring Boot Application](https://www.baeldung.com/spring-boot-opentelemetry-setup)

# how to run it

## Replace XXXXX by Player Zero API key

In spring-cloud-open-telemetry1/src/main/resources/application.properties and spring-cloud-open-telemetry2/src/main/resources/application.properties replace XXXXX by the Player Zero API key.

## Run the application

```bash
cd spring-cloud-modules/spring-cloud-open-telemetry
mvn clean install
docker-compose up
```

## Try the application

```
GET http://localhost:8080/product/100003
```

You'll see in the logs the following error:

```
product-service-1  | 2024-06-04 16:42:25.074  WARN [product-service,,] 1 --- [yerzero.app/...] i.o.e.internal.grpc.OkHttpGrpcExporter   : Failed to export spans. Server responded with HTTP status code 464. Error message:
```
