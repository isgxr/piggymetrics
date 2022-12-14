FROM docker-registry-idc01-sz.cloudtogo.cn/cloudtogo/openjdk:8-jre
#FROM java:8-jre
MAINTAINER Chi Dov <d.chiproeng@gmail.com>
WORKDIR /workspace
ADD ./target/turbine-stream-service.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/turbine-stream-service.jar"]

EXPOSE 8989
