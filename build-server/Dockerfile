FROM ubuntu:20.04
RUN apt update
RUN apt install git -y
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt install default-jdk -y
RUN apt install maven -y
RUN apt install curl -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR boxfuse-sample-java-war-hello/
RUN mvn package

EXPOSE 8080
#RUN cp /boxfuse-sample-java-war-hello/target/hello-1.0.war /opt/tomcat/webapps/
#CMD ["/opt/tomcat/bin/catalina.sh", "run"]
CMD ["/bin/bash"]