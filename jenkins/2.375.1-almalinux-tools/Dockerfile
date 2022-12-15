FROM jenkins/jenkins:2.375.1-almalinux
USER root
RUN dnf install -y rpm-build python3 subversion ant
RUN pip3 install plumbum
USER jenkins
VOLUME [/opt/mdc-installer-tool]
