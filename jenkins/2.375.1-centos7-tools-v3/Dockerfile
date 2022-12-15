FROM jenkins/jenkins:2.375.1-lts-centos7
USER root
RUN yum install epel-release
RUN yum clean all  \
    && yum install -y rpm-build python3 subversion python-plumbum
USER jenkins
