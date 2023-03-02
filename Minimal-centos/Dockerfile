FROM python:3.8-slim
RUN mkdir -p /mobilityzone
WORKDIR /mobilityzone
COPY . /mobilityzone
RUN pip3 install flask 
EXPOSE 80
EXPOSE 8080
ENTRYPOINT ["python3" , "mobility_was.py"]


 
