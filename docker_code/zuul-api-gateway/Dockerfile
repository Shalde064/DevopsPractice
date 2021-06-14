#Build stage
FROM maven as build
WORKDIR /app
COPY . .
RUN mvn clean install

#Package stage
FROM openjdk
WORKDIR /app
COPY --from=build app/target/zuul-0.0.1-SNAPSHOT.jar /app
EXPOSE 9999
CMD ["java","-jar","zuul-0.0.1-SNAPSHOT.jar"]
