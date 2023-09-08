FROM registry.access.redhat.com/ubi8 
ENV container docker
WORKDIR /build
RUN curl -L https://cbs.centos.org/kojifiles/packages/systemd/249/1.20210731.e370962.hs.el8/x86_64/systemd-249-1.20210731.e370962.hs.el8.x86_64.rpm -o systemd-249-1.rpm
RUN rpm -Uvh --force --nodeps systemd-249-1.rpm
RUN yum install iptables-libs -y
RUN rm -rvf /build && yum clean all
VOLUME [ "/sys/fs/cgroup" ]
CMD ["/usr/sbin/init"]
