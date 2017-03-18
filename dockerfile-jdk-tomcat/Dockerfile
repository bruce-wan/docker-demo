# Pull base image  
FROM ubuntu  
  
MAINTAINER zing wang "zing.jian.wang@gmail.com"   
  
# Install JDK 7
ADD ./jdk-7u80-linux-x64.tar.gz /opt
  
# Install tomcat7  
ADD ./apache-tomcat-8.5.12.tar.gz /opt

ENV JAVA_HOME /opt/jdk1.7.0_80
ENV CATALINA_HOME /opt/apache-tomcat-8.5.12  
ENV PATH $PATH:$JAVA_HOME/bin:

VOLUME ["/opt/apache-tomcat-8.5.12/webapps/"]

# Expose ports.  
EXPOSE 8080

# Define default command.  
ENTRYPOINT /opt/apache-tomcat-8.5.12/bin/startup.sh && tail -F /opt/apache-tomcat-8.5.12/logs/catalina.out
