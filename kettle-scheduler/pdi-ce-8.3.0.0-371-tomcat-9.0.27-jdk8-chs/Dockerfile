FROM opsu/tomcat:9.0.27-jdk8-chs

MAINTAINER yxf521@gmail.com

RUN apt-get clean && apt-get update \
    && apt-get install --fix-missing -y wget

WORKDIR /usr/local/tomcat/
RUN wget http://192.168.119.1/pdice/pdi-ce-8.3.0.0-371.zip \
    && unzip pdi-ce-8.3.0.0-371.zip && rm -rf pdi-ce-8.3.0.0-371.zip\
    && cp -r data-integration/system/ data-integration/simple-jndi/ .

# docker build -t opsu/kettle-scheduler-process:pdi-ce-8.3.0.0-371 .
