FROM debian:stretch

ENV TZ='Asia/Shanghai'
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        apt-transport-https \
        ca-certificates \
        tzdata \
    && sed -i "s@http://.*.debian.org@https://mirrors.ustc.edu.cn@g" /etc/apt/sources.list \
    && rm -rf /var/apt/cache/*
