FROM centos:6.8
USER root

COPY subversion_installer_1.7.sh .
COPY get-pip.py .

RUN sed -i 's/mirror.centos.org\/centos\/\$releasever/vault.centos.org\/6.8/' /etc/yum.repos.d/CentOS-Base.repo \ 
    && sed -i 's/mirrorlist/\#mirrorlist/' /etc/yum.repos.d/CentOS-Base.repo \ 
    && sed -i 's/\#baseurl/baseurl/' /etc/yum.repos.d/CentOS-Base.repo

RUN yum install -qy epel-release \ 
    && yum install -qy ant rpm-build python34

RUN python3 get-pip.py \
    && rm -f get-pip.py \ 
    && pip install plumbum

RUN export NON_INTERACTIVE=1 \ 
    && bash subversion_installer_1.7.sh
