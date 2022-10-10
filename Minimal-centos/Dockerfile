FROM centos:centos7
RUN mkdir -p /mobilityzone
WORKDIR /mobilityzone
COPY . /mobilityzone
RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
##RUN yum update -y 
RUN yum install centos-release-scl
RUN yum install rh-python36
RUN scl enable rh-python36 bash
RUN mkdir my_flask_app cd my_flask_app
RUN python3 -m venv venv
RUN source venv/bin/activate
RUN pip install Flask
##RUN yum install python3 -y
##RUN yum install python3-pip -y
##RUN yum install flask
EXPOSE 80
EXPOSE 8080
ENTRYPOINT ["python3" , "mobility_was.py"]
