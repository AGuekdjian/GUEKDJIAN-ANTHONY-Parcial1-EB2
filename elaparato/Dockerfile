FROM openjdk:17-alpine
RUN apk update && apk add maven
WORKDIR /app
COPY . .
RUN mvn package && mvn clean install -DskipTests
CMD ["java", "-jar", "target/elaparato-0.0.1-SNAPSHOT.jar"]