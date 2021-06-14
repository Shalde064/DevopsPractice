#Build stage
FROM maven as build
RUN mkdir /app
WORKDIR /app
COPY . .
RUN mvn clean install

#Package stage
FROM openjdk
RUN mkdir /app
WORKDIR /app
COPY --from=build app/target/offers-0.0.1-SNAPSHOT.jar /app
EXPOSE 1001
CMD ["java","-jar","offers-0.0.1-SNAPSHOT.jar"]
