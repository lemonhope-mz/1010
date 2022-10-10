FROM centos7:latest
RUN mkdir -p /mobilityzone
WORKDIR /mobilityzone
COPY . /mobilityzone
RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
##RUN yum update -y 
RUN yum install python3 -y
RUN yum install python3-pip -y
RUN yum install flask
EXPOSE 80
EXPOSE 8080
ENTRYPOINT ["python3" , "mobility_was.py"]
