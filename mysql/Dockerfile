ARG MYSQL_VERSION
FROM mysql:${MYSQL_VERSION}

### set timezome
ENV TZ=Asia/Shanghai
# mysql镜像采用Debian GNU/Linux 9 设置系统时区很方便
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone