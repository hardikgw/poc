FROM ubuntu:14.04
MAINTAINER hardik.patel@cbp.dhs.gov
RUN apt-get update
RUN apt-get install -y vim curl wget
RUN wget https://packages.chef.io/stable/ubuntu/14.04/chef-server-core_12.6.0-1_amd64.deb 
RUN sudo dpkg -i chef-server-core_12.6.0-1_amd64.deb
RUN apt-get update
RUN chef-server-ctl reconfigure
EXPOSE 80 443
