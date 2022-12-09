FROM docker-registry-idc01-sz.cloudtogo.cn/cloudtogo/cloudos-maven:3.6.3-openjdk-8-202108051122 AS builder
WORKDIR /workspace
#ENV MAVEN_NEXUS_REPO=http://maven.aliyun.com/repository/public
#RUN mkdir ~/.m2 && wget --tries=1 -O ~/.m2/settings.xml http://share.devops.cloud2go.cn/dev/cloud-ide/extension/java/settings.xml 
RUN mvn clean package -s ~/.m2/settings.xml -Dmaven.test.skip=true
FROM docker-registry-idc01-sz.cloudtogo.cn/cloudtogo/openjdk:8-jre
COPY --from=builder /workspace/config/target/config.jar /home/
WORKDIR /home
ENV JAVA_OPTS=" -Xms256m -Xmx256m"
CMD java ${JAVA_OPTS} -jar *.jar
