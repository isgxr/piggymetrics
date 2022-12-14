FROM docker-registry-idc01-sz.cloudtogo.cn/cloudtogo/openjdk:8-jre
#FROM java:8-jre
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>
WORKDIR /workspace
ADD ./target/registry.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/registry.jar"]

EXPOSE 8761
