FROM ubuntu
RUN apt update
WORKDIR /mnt/
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz .
RUN tar -xvf apache-tomcat-9.0.93.tar.gz 
RUN apt install openjdk-11-jdk -y
ADD https://erp-student-application.s3.ap-northeast-1.amazonaws.com/student.war ./apache-tomcat-9.0.93/webapps/
ADD https://erp-student-application.s3.ap-northeast-1.amazonaws.com/mysql-connector.jar ./apache-tomcat-9.0.93/lib/
ADD https://erp-student-application.s3.ap-northeast-1.amazonaws.com/context.xml ./apache-tomcat-9.0.93/conf/
EXPOSE 8080
CMD [ "./apache-tomcat-9.0.93/bin/catalina.sh", "run" ]
