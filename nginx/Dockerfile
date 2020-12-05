ARG NGINX_VERSION
FROM nginx:${NGINX_VERSION}-alpine

### set timezome
ENV TZ=Asia/Shanghai
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    # nginx基础镜像需要apk update
    && apk update && apk add tzdata \
    && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone