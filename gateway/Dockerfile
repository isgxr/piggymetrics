FROM docker-registry-idc01-sz.cloudtogo.cn/cloudtogo/openjdk:8-jre
#FROM java:8-jre
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>

ADD ./target/gateway.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/gateway.jar"]

EXPOSE 4000
