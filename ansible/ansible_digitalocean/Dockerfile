FROM alpine

RUN apk update
# RUN addgroup -S alpine_group
# RUN adduser -S alpine_user -G alpine_group
RUN apk add openssh
RUN apk add -u ansible
RUN apk add py-pip
RUN pip install 'dopy==0.3.7'

COPY . /
ADD ./.ssh /root/.ssh
RUN chmod 400 ~/.ssh/id_rsa
RUN  chmod -x password

RUN ansible-playbook --vault-password-file=password ./digitalocean/play.yml