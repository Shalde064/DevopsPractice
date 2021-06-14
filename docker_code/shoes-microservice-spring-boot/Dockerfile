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
COPY --from=build app/target/shoes-0.0.1-SNAPSHOT.jar /app
EXPOSE 1002
CMD ["java","-jar","shoes-0.0.1-SNAPSHOT.jar"]
