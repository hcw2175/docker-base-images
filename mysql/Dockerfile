# 基于 mysql:5.7 镜像
FROM mysql:5.7

# 维护者：iotp-hucw<hcw2175@163.com>
MAINTAINER iotp-hucw<hcw2175@163.com>

# 覆盖 server.xml 配置文件
COPY ./mysql-usr.cnf /etc/mysql/conf.d/mysql-usr.cnf

# 覆盖时区
COPY ./localtime /etc/localtime

# 设置中文
ENV LANG=C.UTF-8

# 暴露端口 3306
EXPOSE 3306

# 运行命令
CMD ["mysqld"]
