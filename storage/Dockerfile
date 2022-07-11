FROM centos:7

ENV CEPH_VERSION "nautilus"
RUN wget -O /etc/yum.repos.d/ceph-nautilus.repo http://10.10.36.12/app/repofile/Ceph-nautilus.repo && \
  yum install -y epel-release && \
  yum install -y --nogpgcheck ceph-common && \
  yum clean all

COPY rbd-provisioner /usr/local/bin/rbd-provisioner
ENTRYPOINT ["/usr/local/bin/rbd-provisioner"]
