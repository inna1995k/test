FROM ubuntu:16.04
RUN apt update
ADD id_rsa /root/.ssh/id_rsa
RUN chmod 700 /root/.ssh/id_rsa
RUN chown -R root:root /root/.ssh
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello
RUN cd boxfuse-sample-java-war-hello
RUN mvn package
RUN boxfuse run target/hello-1.0.war
RUN buxfuse
RUN apt install tomcat7
EXPOSE 8080
CMD service tomcat7 start

