FROM eclipse-temurin:25-jdk-alpine
COPY . /app/examples
WORKDIR /app
RUN javac examples/*.java
RUN jar cfe main.jar examples.HelloJava examples/*.class 
WORKDIR /app
CMD ["java","-jar","main.jar"]
