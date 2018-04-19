# 基于 omcat:8.5-jre8 镜像
From tomcat:8.5-jre8

# 维护者：iotp-hucw<hcw2175@163.com>
MAINTAINER iotp-hucw<hcw2175@163.com>

# 覆盖 server.xml 配置文件
COPY server.xml /usr/local/tomcat/conf/server.xml

# 覆盖时区
COPY localtime /etc/localtime

# 设置 java 运行内存、时区
# ENV JAVA_OPTS -server -Xmx1G -Xms1G -Xmn200M -Duser.timezone=GMT+08
ENV JAVA_OPTS -server -Duser.timezone=GMT+08

# 更新软索引并安装 nano 工具
# RUN apt-get update &&  apt-get install nano 

# 暴露端口 8080
EXPOSE 8080

# 运行命令
CMD ["catalina.sh", "run"]
