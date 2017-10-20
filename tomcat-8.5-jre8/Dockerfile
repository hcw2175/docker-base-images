From tomcat:8.5-jre8
MAINTAINER iotp-hucw<hcw2175@163.com>
COPY server.xml /usr/local/tomcat/conf/server.xml
COPY localtime /etc/localtime
ENV JAVA_OPTS -server -Xms2048M -Xmx2048M -Xmn200M -XX:PermSize=256M -XX:MaxPermSize=256M -Duser.timezone=GMT+08
RUN apt-get update &&  apt-get install nano
EXPOSE 8080
CMD ["catalina.sh", "run"]
