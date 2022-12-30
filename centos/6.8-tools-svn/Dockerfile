FROM centos:6.8
USER root

COPY subversion_installer_1.7.sh .
COPY get-pip.py .

RUN sed -i 's/mirror.centos.org\/centos\/\$releasever/vault.centos.org\/6.8/' /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i 's/mirrorlist/\#mirrorlist/' /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i 's/\#baseurl/baseurl/' /etc/yum.repos.d/CentOS-Base.repo

RUN yum install -y epel-release
RUN yum install -y ant rpm-build epel-release python34

RUN python3 get-pip.py 
RUN rm -f get-pip.py
RUN pip install plumbum

RUN export NON_INTERACTIVE=1 && bash subversion_installer_1.7.sh
