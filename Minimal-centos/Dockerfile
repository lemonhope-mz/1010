FROM centos:latest
RUN mkdir -p /mobilityzone
WORKDIR /mobilityzone
COPY . /mobilityzone
##RUN yum update -y 
RUN yum install python3 -y
RUN yum install python3-pip -y
RUN yum install flask
EXPOSE 80
EXPOSE 8080
ENTRYPOINT ["python3" , "mobility_was.py"]
