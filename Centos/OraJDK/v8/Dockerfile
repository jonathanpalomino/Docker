FROM centos:latest
MAINTAINER Jonathan Palomino <jonathan.palomino.vilca@gmail.com>

# get updates via yum
RUN yum -y upgrade && \
    yum -y update && \
    yum -y install wget unzip findutils && \
    yum clean all

ENV VERSION 8
ENV UPDATE 144
ENV SIG 090f390dda5b47b9b721c7dfaa008135
ENV BUILD 1

# test
#RUN cd /opt && \
#    curl -j -k -L -H "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u144-b01/090f390dda5b47b9b721c7dfaa008135/jdk-8u144-linux-x64.tar.gz | tar xz

RUN mkdir -p /usr/lib/jvm && \ cd /usr/lib/jvm && \
	 curl -j -k -L -H "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/"${VERSION}"u"${UPDATE}"-b"${BUILD}"/"${SIG}"/jdk-"${VERSION}"u"${UPDATE}"-linux-x64.tar.gz | tar xz


#RUN alternatives --install /usr/bin/java java /opt/jdk1.${VERSION}.0_${UPDATE}/bin/java 2 && \
#    alternatives --install /usr/bin/javac javac /opt/jdk1.${VERSION}.0_${UPDATE}/bin/javac 2 && \
#    alternatives --install /usr/bin/jar jar /opt/jdk1.${VERSION}.0_${UPDATE}/bin/jar 2
	
RUN alternatives --install /usr/bin/java java /usr/lib/jvm/jdk1.${VERSION}.0_${UPDATE}/bin/java 2 && \
    alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk1.${VERSION}.0_${UPDATE}/bin/javac 2 && \
    alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk1.${VERSION}.0_${UPDATE}/bin/jar 2

ENV JAVA_HOME /usr/lib/jvm/jdk1.${VERSION}.0_${UPDATE}

ENV JRE_HOME=/usr/lib/jvm/jdk1.${VERSION}.0_${UPDATE}/jre
#ENV PATH=$PATH:/opt/jdk1.8.0_144/bin:/opt/jdk1.8.0_144/jre/bin
ENV PATH=$PATH:${JAVA_HOME}/bin:${JRE_HOME}/bin

ENV HOME /root

WORKDIR /root

CMD ["/bin/bash"]

