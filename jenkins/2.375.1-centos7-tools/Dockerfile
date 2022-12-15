FROM jenkins/jenkins:2.375.1-lts-centos7
USER root
RUN yum install -y rpm-build python3 subversion ant
RUN pip3 install plumbum
USER jenkins
VOLUME [/opt/mdc-installer-tool]
