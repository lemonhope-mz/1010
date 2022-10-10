FROM ubuntu:latest
RUN mkdir -p /mobilityzone
WORKDIR /mobilityzone
COPY . /mobilityzone
RUN Fix apt-get update “the following signatures couldn’t be verified because the public key is not available”
##RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 871920D1991BC93C
RUN apt update && apt upgrade -y 
RUN apt install software-properties-common -y
RUN add-apt-repository ppa:deadsnakes/ppa -y
RUN apt install python3.10 -y
RUN apt install python3-pip -y
RUN pip install flask
EXPOSE 80
EXPOSE 8080
ENTRYPOINT ["python3" , "mobility_was.py"]
