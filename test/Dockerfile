FROM centos:7
MAINTAINER Rajesh M "rajesh.m01@sap.com"

# Adding Repo file .. keep your repo files inside 'repo' directory 

ADD ./repo /etc/yum.repos.d/

#installing httpd and net-tools 

RUN yum update -y && yum clean all && yum install httpd -y
RUN yum install net-tools -y 

#Creating index.htmlfile 

RUN echo "This is a test Website URL written for Docker testing" >> /var/www/html/index.html

#Exposing port 443 and 80 

EXPOSE 80 443

# Start the service as deamon inside the docker ( This will run in detached mode ) 
CMD ["-D", "FOREGROUND"]
ENTRYPOINT ["/usr/sbin/httpd"]


