FROM debian:buster

ENV TZ='Asia/Shanghai'
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        apt-transport-https \
        ca-certificates \
        tzdata \
    && rm -rf /var/apt/cache/*

COPY ./sources.list /etc/apt/sources.list
