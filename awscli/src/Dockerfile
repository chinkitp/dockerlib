FROM python:3.6.5-alpine3.7

RUN pip install awscli \
    && apk update \
    && apk add openssh

ADD ./.ssh /root/.ssh
RUN chmod 400 ~/.ssh/id_rsa
