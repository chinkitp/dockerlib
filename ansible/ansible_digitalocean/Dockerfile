FROM alpine

RUN apk update
# RUN addgroup -S alpine_group
# RUN adduser -S alpine_user -G alpine_group
RUN apk add openssh
RUN apk add -u ansible
RUN apk add py-pip
RUN pip install 'dopy==0.3.7'
RUN ansible-galaxy install geerlingguy.java
RUN ansible-galaxy install geerlingguy.elasticsearch

COPY . /
ADD ./.ssh /root/.ssh
RUN chmod 400 ~/.ssh/id_rsa
