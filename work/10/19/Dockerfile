FROM docker.io/centos:latest
ADD hello-docker.txt /tmp
RUN cd /etc/yum.repos.d/; sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*; sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN yum clean all
RUN yum update -y
RUN yum install -y epel-release
CMD ["/bin/bash"]
