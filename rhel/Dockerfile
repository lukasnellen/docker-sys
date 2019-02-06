ARG baseimage=centos:6
FROM $baseimage

LABEL maintainers="Lukas Nellen <lukas@nucleares.unam.mx>" \
      name="Software install environment" 

# set yum to dnf for fedora images
ARG yum=yum

# set mysqldevel to
#    mysql-devel for CentOS 6,
#    mariadb-devel for Centos7
#    community-mysql-devel for Fedora 27, 28
ARG mysqldevel=mariadb-devel

RUN $yum install -y \ 
# build tools and helper
    binutils \
    findutils \
    doxygen \
    gcc \
    gcc-c++ \
    gcc-gfortran \
    git \
    less \
    make \
#    awk \ # awk installed
    patch \
    python \
    python-devel \
    python-virtualenv \
    rsync \
    subversion \
    which \
    file \
# build dependencies
    bzip2-devel \
    libX11-devel \
    libXpm-devel \
    libXft-devel \
    libXext-devel \
    zlib-devel \
    $mysqldevel \
    openssl \
# for running final software
    wget \
  && \
# cleanup
    $yum clean all && rm -rf /var/cache/yum
