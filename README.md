# docker-tomcat-cn

适用于国内大部分 Java 应用的 docker tomcat

基于官方 `tomcat:8.5-jre8` 镜像构建，新增特性如下：

* 优化server.xml配置，如增加连接超时、最大线程数等
* 优化 JDK 内存配置：-server -Xmx1G -Xms1G -Xmn200M -Duser.timezone=GMT+08
* 增加中国时区配置
* 增加 nano 编辑工具

# Docker Hub 地址

[https://hub.docker.com/r/hucw/tomcat/](https://hub.docker.com/r/hucw/tomcat/)
