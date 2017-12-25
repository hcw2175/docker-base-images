# 基于nginx构建
FROM nginx

# 维护者
MAINTAINER hcw2175<hcw2175@163.com>

# 覆盖默认配置文件
COPY ./nginx.conf /etc/nginx/nginx.conf

# 复制vue项目配置配置文件
COPY ./nginx-vue.conf /etc/nginx/conf.d/default.conf

# 安装 nano 工具
# RUN apt-get clean && apt-get update --fix-missing && apt-get install nano \

# 使用 nginxusr 用户运行
# USER nginxusr