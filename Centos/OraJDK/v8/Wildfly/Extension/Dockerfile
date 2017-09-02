FROM centos7_jdk8_wildfly10:latest

EXPOSE 9990

RUN /opt/jboss/wildfly/wildfly-10.1.0.Final/bin/add-user.sh admin 7@jonathan --silent
CMD ["/opt/jboss/wildfly/wildfly-10.1.0.Final/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0"]

