FROM centos:7.5.1804
MAINTAINER Richard <nibocn@gmail.com>

ARG JAVA_VERSION=8u171

RUN cd /tmp \
    && mkdir -p /opt/java \
    && curl -o jre-${JAVA_VERSION}-linux-x64.tar.gz -L -O -H "Cookie: oraclelicense=accept-securebackup-cookie" -k "http://ftp.wsisiz.edu.pl/pub/pc/pozyteczne%20oprogramowanie/java/${JAVA_VERSION}/jre-${JAVA_VERSION}-linux-x64.tar.gz" \
    && tar xf jre-${JAVA_VERSION}-linux-x64.tar.gz -C /opt/java \
    && rm -rf jre-${JAVA_VERSION}-linux-x64.tar.gz \
    && ln -s /opt/java/jre* /opt/java/jre \
    && ln -s /opt/java/jre /opt/java/jvm \
    && ln -s /opt/java/jre/bin/java /usr/local/bin \
    && rm -rf /opt/java/jre/lib/desktop

ENV JAVA_HOME /opt/java/jre
ENV PATH $JAVA_HOME/bin:$PATH
