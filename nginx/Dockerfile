# 基于nginx构建
FROM nginx

# 维护者
MAINTAINER hcw2175<hcw2175@163.com>

# 覆盖默认配置文件
COPY ./nginx.conf /etc/nginx/nginx.conf

# 复制vue项目配置配置文件
COPY ./nginx-vue.conf /etc/nginx/conf.d/default.conf

# 设置国内源
RUN sed -i 's#http://archive.ubuntu.com#http://mirrors.163.com#g' /etc/apt/sources.list

# 安装 nano 工具
# 新增文件 touch /var/run/nginx.pid
# 添加 nginxusr:nginxusr 用户
# 授权目录文件
# apt-get clean && apt-get update --fix-missing && apt-get install nano \
RUN touch /var/run/nginx.pid \
    && groupadd -g 2000 nginxusr && useradd -u 2000 -g nginxusr -m -s /bin/bash nginxusr \
    && chown -R nginxusr:nginxusr /var/run/nginx.pid \
    && chown -R nginxusr:nginxusr /etc/nginx \
    && chown -R nginxusr:nginxusr /var/cache/nginx \
    && chown -R nginxusr:nginxusr /var/log/nginx \
    && chown -R nginxusr:nginxusr /usr/share/nginx/html

# 使用 nginxusr 用户运行
USER nginxusr

# 暴露端口 8080
EXPOSE 8080