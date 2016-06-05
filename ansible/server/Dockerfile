FROM ubuntu:14.04
MAINTAINER hardik.patel@cbp.dhs.gov
RUN apt-get update
RUN apt-get install -y vim curl wget
RUN apt-get update && \
    apt-get install --no-install-recommends -y software-properties-common && \
    apt-add-repository ppa:ansible/ansible && \
    apt-get update && \
    apt-get install -y ansible

RUN echo '[local]\nlocalhost\n' > /etc/ansible/hosts
