ARG baseimage=debian:stretch
FROM $baseimage

# on ubuntu, try: libmysqlclient-dev
ARG mysqlclientdev=default-libmysqlclient-dev

LABEL maintainers="Lukas Nellen <lukas@nucleares.unam.mx>" \
      name="Software install environment" 

RUN apt-get update && \
    apt-get install --no-install-recommends --yes \ 
# build tools and helpers
    binutils \
    debianutils \
    dpkg-dev \
    doxygen \
    gcc \
    g++ \
    gfortran \
    git \
    less \
    make \
#    awk \ # mawk installed
    patch \
    python \
    rsync \
    subversion \
    python-virtualenv \
    openssl \
#    which \ # debianutils
    file \
# package headers
    libbz2-dev \
    libpng-dev \
    libjpeg-dev \
    $mysqlclientdev \
    libx11-dev \
    libxpm-dev \
    libxft-dev \
    libxext-dev \
    python-dev \
    zlib1g-dev \
# for running final software
    wget \
  && \
# cleanup
    apt-get clean && rm -rf /var/lib/apt/lists/*

