FROM centos:7.5.1804
MAINTAINER Richard <nibocn@gmail.com>

ARG JAVA_VERSION=8u171

RUN cd /tmp \
    && mkdir -p /opt/java \
    && curl -o jdk-${JAVA_VERSION}-linux-x64.tar.gz -L -O -H "Cookie: oraclelicense=accept-securebackup-cookie" -k "http://ftp.wsisiz.edu.pl/pub/pc/pozyteczne%20oprogramowanie/java/${JAVA_VERSION}/jdk-${JAVA_VERSION}-linux-x64.tar.gz" \
    && tar xf jdk-${JAVA_VERSION}-linux-x64.tar.gz -C /opt/java \
    && rm -rf jdk-${JAVA_VERSION}-linux-x64.tar.gz \
    && ln -s /opt/java/jdk* /opt/java/jdk \
    && ln -s /opt/java/jdk /opt/java/jvm \
    && ln -s /opt/java/jdk/bin/java /usr/local/bin \
    && ln -s /opt/java/jdk/bin/javac /usr/local/bin \
    && yum clean all \
    && rm -rf /tmp/* \
    /opt/java/jdk/*src.zip \
    /opt/java/jdk/lib/missioncontrol \
    /opt/java/jdk/lib/visualvm \
    /opt/java/jdk/lib/*javafx* \
    /opt/java/jdk/jre/plugin \
    /opt/java/jdk/jre/bin/javaws \
    /opt/java/jdk/jre/bin/jjs \
    /opt/java/jdk/jre/bin/orbd \
    /opt/java/jdk/jre/bin/pack200 \
    /opt/java/jdk/jre/bin/policytool \
    /opt/java/jdk/jre/bin/rmid \
    /opt/java/jdk/jre/bin/rmiregistry \
    /opt/java/jdk/jre/bin/servertool \
    /opt/java/jdk/jre/bin/tnameserv \
    /opt/java/jdk/jre/bin/unpack200 \
    /opt/java/jdk/jre/lib/javaws.jar \
    /opt/java/jdk/jre/lib/deploy* \
    /opt/java/jdk/jre/lib/desktop \
    /opt/java/jdk/jre/lib/*javafx* \
    /opt/java/jdk/jre/lib/*jfx* \
    /opt/java/jdk/jre/lib/amd64/libdecora_sse.so \
    /opt/java/jdk/jre/lib/amd64/libprism_*.so \
    /opt/java/jdk/jre/lib/amd64/libfxplugins.so \
    /opt/java/jdk/jre/lib/amd64/libglass.so \
    /opt/java/jdk/jre/lib/amd64/libgstreamer-lite.so \
    /opt/java/jdk/jre/lib/amd64/libjavafx*.so \
    /opt/java/jdk/jre/lib/amd64/libjfx*.so \
    /opt/java/jdk/jre/lib/ext/jfxrt.jar \
    /opt/java/jdk/jre/lib/ext/nashorn.jar \
    /opt/java/jdk/jre/lib/oblique-fonts \
    /opt/java/jdk/jre/lib/plugin.jar


ENV JAVA_HOME /opt/java/jdk
ENV PATH $JAVA_HOME/bin:$PATH
