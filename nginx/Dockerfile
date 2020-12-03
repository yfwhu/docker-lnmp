ARG NGINX_VERSION
FROM nginx:${NGINX_VERSION}-alpine

### set timezome
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

