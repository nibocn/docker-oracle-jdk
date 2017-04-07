FROM nibo/centos:7.3.1611
MAINTAINER Richard <nibocn@gmail.com>

RUN cd /tmp \
    && mkdir -p /opt/java \
    && curl -L -O -H "Cookie: oraclelicense=accept-securebackup-cookie" -k "http://download.oracle.com/otn-pub/java/jdk/8u112-b15/jre-8u112-linux-x64.tar.gz" \
    && tar xf jre-8u112-linux-x64.tar.gz -C /opt/java \
    && rm -rf jre-8u112-linux-x64.tar.gz \
    && ln -s /opt/java/jre* /opt/java/jre \
    && ln -s /opt/java/jre /opt/java/jvm

ENV JAVA_HOME /opt/java/jre
ENV PATH $JAVA_HOME/bin:$PATH
