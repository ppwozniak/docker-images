FROM jenkins/jenkins:2.375.1-lts-centos7
USER root
RUN yum clean all  \
    && yum-config-manager --disable github_git-lfs* \
    && yum install -y rpm-build python3 subversion
USER jenkins
