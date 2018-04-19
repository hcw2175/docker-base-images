# 基于openjdk的8u131-jre版本构建
FROM openjdk:8u131-jre

# 维护者
MAINTAINER hucw

# Java环境变量
#ENV JAVA_OPTS="-server -Xmx1G -Xms1G -Xmn200M -Duser.timezone=GMT+08"

# 容器运行执行命令
# 默认运行 /jar/app.jar
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -jar /jar/app.jar" ]