FROM openjdk:8-jdk-alpine

WORKDIR /desafio-um-pfa

COPY desafio-um-pfa-1.0.0.jar .

RUN apk add --no-cache openssl

ENV DOCKERIZE_VERSION v0.6.1

EXPOSE 8080

RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz

# ENTRYPOINT ["java", "-jar", "desafio-um-pfa-1.0.0.jar"]