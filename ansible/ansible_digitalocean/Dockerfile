FROM ubuntu:16.04

RUN apt-get --yes update \
    && apt-get --yes install software-properties-common \
    && apt-add-repository --yes ppa:ansible/ansible \
    && apt-get --yes update \
    && apt-get --yes install ansible \
    && apt-get --yes install python-pip \
    && pip install 'dopy>=0.3.2'

COPY . /

RUN ansible-playbook ./digitalocean/play.yml