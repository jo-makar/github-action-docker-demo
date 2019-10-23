FROM centos:7

RUN yum -y update && yum -y install git

RUN rpm --import https://mirror.go-repo.io/centos/RPM-GPG-KEY-GO-REPO && \
    (cd /etc/yum.repos.d/; curl -Os https://mirror.go-repo.io/centos/go-repo.repo) && \
    yum -y install golang

COPY run.sh /
CMD /run.sh
