FROM jdk8_144 
MAINTAINER Jonathan Palomino <jonathan.palomino.vilca@gmail.com>
ADD https://services.gradle.org/distributions/gradle-4.1-bin.zip /tmp/gradle-4.1-bin.zip
RUN apt-get install zip -y \ unzip /tmp/gradle-4.1-bin.zip -d /tmp && cp -R /tmp/gradle-4.1/* /usr/local/ && rm -Rf /tmp/gradle-4.1 /tmp/gradle-4.1-bin.zip
