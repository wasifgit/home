FROM openjdk:8-jdk-alpine
RUN apk --no-cache add curl
#COPY target/JavaSamples*.jar JavaSamples.jar
COPY build/libs/*-all.jar JavaSamples.jar
EXPOSE 8080
CMD java -XX:+UnlockExperimentalVMOptions -XX:+UseCGroupMemoryLimitForHeap \
    -Dcom.sun.management.jmxremote -noverify ${JAVA_OPTS} -jar JavaSamples.jar
