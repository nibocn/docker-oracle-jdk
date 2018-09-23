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
    && yum clean all \
    && rm -rf /tmp/* \
    /opt/java/jre/plugin \
    /opt/java/jre/bin/javaws \
    /opt/java/jre/bin/jjs \
    /opt/java/jre/bin/orbd \
    /opt/java/jre/bin/pack200 \
    /opt/java/jre/bin/policytool \
    /opt/java/jre/bin/rmid \
    /opt/java/jre/bin/rmiregistry \
    /opt/java/jre/bin/servertool \
    /opt/java/jre/bin/tnameserv \
    /opt/java/jre/bin/unpack200 \
    /opt/java/jre/lib/javaws.jar \
    /opt/java/jre/lib/deploy* \
    /opt/java/jre/lib/*jfx* \
    /opt/java/jre/lib/amd64/libdecora_sse.so \
    /opt/java/jre/lib/amd64/libprism_*.so \
    /opt/java/jre/lib/amd64/libfxplugins.so \
    /opt/java/jre/lib/amd64/libglass.so \
    /opt/java/jre/lib/amd64/libgstreamer-lite.so \
    /opt/java/jre/lib/amd64/libjavafx*.so \
    /opt/java/jre/lib/amd64/libjfx*.so \
    /opt/java/jre/lib/ext/jfxrt.jar \
    /opt/java/jre/lib/ext/nashorn.jar \
    /opt/java/jre/lib/oblique-fonts \
    /opt/java/jre/lib/plugin.jar


ENV JAVA_HOME /opt/java/jre
ENV PATH $JAVA_HOME/bin:$PATH
