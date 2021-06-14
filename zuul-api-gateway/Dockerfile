#Build stage
FROM maven as build
RUN mkdir /app
WORKDIR /app
COPY . .
RUN mvn clean install

#Package stage
FROM openjdk:8-jdk-alpine
RUN mkdir /app
WORKDIR /app
COPY --from=build /app/zuul-0.0.1-SNAPSHOT.jar /app
EXPOSE 9999
CMD ["java","-jar","zuul-0.0.1-SNAPSHOT.jar"]
