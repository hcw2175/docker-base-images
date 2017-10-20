# 基于openjdk的8u131-jre版本构建
FROM openjdk:8u131-jre
# 维护者
MAINTAINER iotp-hucw<hcw2175@163.com>
# Java环境变量
ENV JAVA_OPTS="-server -Xmx1G -Xms1G -Xmn200M -Duser.timezone=GMT+08"
# 安装 nano 工具
RUN apt-get update &&  apt-get install nano