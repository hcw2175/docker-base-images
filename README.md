# Docker 基础镜像集合

# Tomcat

[hucw/tomcat 仓库地址](https://hub.docker.com/r/hucw/tomcat/)

适用于国内大部分 Java 应用的 docker tomcat

基于官方 `tomcat:8.5-jre8` 镜像构建，新增特性如下：

* 优化server.xml配置，如增加连接超时、最大线程数等
* 优化 JDK 内存配置：`-server -Xmx1G -Xms1G -Xmn200M -Duser.timezone=GMT+08`
* 增加中国时区配置
* 增加 nano 编辑工具
* 增加普通用户 `tomcat`，用户 uid=2000，并使用 tomcat 用户来启动应用



# OpenJDK

[hucw/openjdk 仓库地址](https://hub.docker.com/r/hucw/openjdk/)

基于官方 `openjdk:8u131-jre` 镜像构建，新增特性如下：

* 优化 JDK 内存配置：`-server -Xmx1G -Xms1G -Xmn200M -Duser.timezone=GMT+08`
* 增加 nano 编辑工具
* 增加普通用户 `jdkusr`，用户 uid=2000，并使用 jdkusr 用户来启动应用




