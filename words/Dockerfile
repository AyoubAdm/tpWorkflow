FROM maven as builder

COPY pom.xml .
RUN mvn verify

COPY src src
RUN mvn verify

FROM openjdk:8-jre-alpine
COPY --from=builder target/ /target

CMD exec java -Xmx256m -Xms128m -jar /target/words.jar
