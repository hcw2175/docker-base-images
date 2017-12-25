# 基于openjdk的8u131-jre版本构建
FROM openjdk:8u131-jre

# 维护者
MAINTAINER iotp-hucw<hcw2175@163.com>

# Java环境变量
ENV JAVA_OPTS="-server -Xmx1G -Xms1G -Xmn200M -Duser.timezone=GMT+08"

# 安装 nano 工具
# 添加 jdkusr 普通用户和组，指定 uid = 2000
# 添加 -R 权限，允许 jdkusr 运行处理
#RUN apt-get update && apt-get install nano \
#RUN groupadd -g 2000 jdkusr \
#    && useradd -u 2000 -g jdkusr -m -s /bin/bash jdkusr \
#    && chown -R jdkusr:jdkusr /docker-java-home \
#    && mkdir -p /rawdatas && chown -R jdkusr:jdkusr /rawdatas && chmod 777 -R /rawdatas

# 使用 jdkusr 用户运行
# USER jdkusr

# 容器运行执行命令
# 默认运行 /jar/app.jar
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -jar /jar/app.jar" ]