# Étape 1 : build avec JDK
FROM eclipse-temurin:21-jdk-alpine AS builder

WORKDIR /app
COPY Main.java .
RUN javac Main.java

# Étape 2 : exécution avec JRE
FROM eclipse-temurin:21-jre-alpine

WORKDIR /app
COPY --from=builder /app/Main.class .

CMD ["java", "Main"]
