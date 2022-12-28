FROM centos:6.8
USER root

RUN sed -i 's/mirror.centos.org\/centos\/\$releasever/vault.centos.org\/6.8/' /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i 's/mirrorlist/\#mirrorlist/' /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i 's/\#baseurl/baseurl/' /etc/yum.repos.d/CentOS-Base.repo

RUN yum install -y subversion ant rpm-build epel-release
RUN yum install -y python34
RUN curl -O https://bootstrap.pypa.io/pip/3.4/get-pip.py
RUN python3 get-pip.py 
RUN rm -f get-pip.py
RUN pip install plumbum
