FROM <AWS ECR URL>/<AWS ECR Repository Name>:update-base-image AS build-env
COPY . /app/examples
WORKDIR /app
RUN javac examples/*.java
RUN jar cfe main.jar examples.HelloJava examples/*.class 

FROM gcr.io/distroless/java25-debian13
COPY --from=build-env /app /app
WORKDIR /app
CMD ["main.jar"]
