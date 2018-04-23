ARG baseimage=centos:6
FROM $baseimage

LABEL maintainers="Lukas Nellen <lukas@nucleares.unam.mx>" \
      name="Software install environment" 

# set yum to dnf for fedora images
ARG yum=yum

RUN $yum upgrade -y \
  && \
    $yum install -y \ 
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
# build dependencies
    bzip2-devel \
    libX11-devel \
    libXpm-devel \
    libXft-devel \
    libXext-devel \
    zlib-devel \
  && \
# cleanup
    $yum clean all && rm -rf /var/cache/yum
