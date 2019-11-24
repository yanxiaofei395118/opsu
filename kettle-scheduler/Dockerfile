FROM opsu/kettle-scheduler-process:pdi-ce-8.3.0.0-371

MAINTAINER yxf521@gmail.com

RUN apt-get clean && apt-get update \
    && apt-get install --fix-missing -y wget

WORKDIR /usr/local/tomcat/webapps/
RUN rm -rf docs examples host-manager manager ROOT \
    && wget http://192.168.119.1/pdice/kettle-scheduler-1.2.0.zip \
    && unzip kettle-scheduler-1.2.0.zip && rm -rf kettle-scheduler-1.2.0.zip

WORKDIR /usr/local/tomcat/
#RUN wget http://192.168.119.1/pdice/pdi-ce-8.3.0.0-371.zip \
#    && unzip pdi-ce-8.3.0.0-371.zip && rm -rf pdi-ce-8.3.0.0-371.zip\
#    && cp -r data-integration/system/ data-integration/simple-jndi/ .

# docker build -t opsu/kettle-scheduler:1.2 .
