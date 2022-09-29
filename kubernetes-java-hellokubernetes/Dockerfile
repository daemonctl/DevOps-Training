FROM maven:3.8.6-openjdk-11
WORKDIR /build
COPY . .
RUN mvn clean package
WORKDIR /build/target
RUN java -jar hello-kubernetes-1.0.0.jar
