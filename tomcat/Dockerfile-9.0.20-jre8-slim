FROM tomcat:9.0.20-jre8-slim

MAINTAINER yxf521@gmail.com

ARG DEBIAN_FRONTEND=noninteractive

# USER root

# RUN echo "deb http://mirrors.aliyun.com/debian/ stretch main non-free contrib"                > /etc/apt/sources.list \
#  && echo "deb-src http://mirrors.aliyun.com/debian/ stretch main non-free contrib"           >> /etc/apt/sources.list \
#  && echo "deb http://mirrors.aliyun.com/debian-security stretch/updates main"                >> /etc/apt/sources.list \
#  && echo "deb-src http://mirrors.aliyun.com/debian-security stretch/updates main"            >> /etc/apt/sources.list \
#  && echo "deb http://mirrors.aliyun.com/debian/ stretch-updates main non-free contrib"       >> /etc/apt/sources.list \
#  && echo "deb-src http://mirrors.aliyun.com/debian/ stretch-updates main non-free contrib"   >> /etc/apt/sources.list \
#  && echo "deb http://mirrors.aliyun.com/debian/ stretch-backports main non-free contrib"     >> /etc/apt/sources.list \
#  && echo "deb-src http://mirrors.aliyun.com/debian/ stretch-backports main non-free contrib" >> /etc/apt/sources.list

RUN apt-get clean && apt-get update \
    && apt-get install --assume-yes --fix-missing apt-utils \
    && apt-get install --fix-missing -y gnupg-agent libreadline7 vim locales ttf-wqy-zenhei ibus ibus-gtk ibus-pinyin

RUN localedef -c -f UTF-8 -i zh_CN zh_CN.utf8 \
 && echo "Asia/Shanghai" > /etc/timezone

# USER tomcat

ENV LANG=zh_CN.utf8
ENV LC_ALL=zh_CN.utf8
