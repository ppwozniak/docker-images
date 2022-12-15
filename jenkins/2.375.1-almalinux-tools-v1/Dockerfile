FROM jenkins/jenkins:2.375.1-almalinux
USER root
RUN dnf clean all  \
    && dnf install -y rpm-build python3 subversion
USER jenkins
