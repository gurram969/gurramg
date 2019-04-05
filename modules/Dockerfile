# docker build -t ubuntu1604py36
FROM ubuntu:16.04

MAINTAINER gurram969@gmail.com

RUN apt-get update && apt-get install -y software-properties-common && add-apt-repository ppa:deadsnakes/ppa && \
    apt-get update && apt-get install -y python3.6 python3.6-dev python3-pip

RUN ln -sfn /usr/bin/python3.6 /usr/bin/python3 && ln -sfn /usr/bin/python3 /usr/bin/python && ln -sfn /usr/bin/pip3 /usr/bin/pip
RUN mkdir -p /opt/modules
WORKDIR /opt/modules
COPY . /opt/modules/
RUN pip install --no-cache-dir  -r requirements.txt
EXPOSE 5000
ENV module_number module_1 module_2 module_3
CMD python 3.6 ./main.py
