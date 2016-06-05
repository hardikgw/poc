FROM ubuntu:14.04
MAINTAINER hardik.patel@cbp.dhs.gov
RUN apt-get update
RUN apt-get install -y vim curl wget
RUN wget https://apt.puppetlabs.com/puppetlabs-release-pc1-wheezy.deb
RUN sudo dpkg -i puppetlabs-release-pc1-wheezy.deb
RUN apt-get update
RUN apt-get install -y puppet-agent
