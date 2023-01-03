FROM centos:6.8
USER root

RUN sed -i 's/mirror.centos.org\/centos\/\$releasever/vault.centos.org\/6.8/' /etc/yum.repos.d/CentOS-Base.repo \ 
    && sed -i 's/mirrorlist/\#mirrorlist/' /etc/yum.repos.d/CentOS-Base.repo \ 
    && sed -i 's/\#baseurl/baseurl/' /etc/yum.repos.d/CentOS-Base.repo

RUN yum install -y epel-release \ 
    && yum install -y rpm-build python34 git

COPY get-pip.py .
RUN python3 get-pip.py \
    && pip install plumbum 

ENV NON_INTERACTIVE=1 NO_MOD_DAV=1
COPY subversion_installer_1.7.sh .
RUN bash subversion_installer_1.7.sh 
