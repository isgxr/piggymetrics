FROM docker-registry-idc01-sz.cloudtogo.cn/cloudtogo/openjdk:8-jre
#FROM java:8-jre
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>
WORKDIR /workspace
ADD ./target/statistics-service.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/statistics-service.jar"]

EXPOSE 7000
