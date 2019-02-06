ARG baseimage=archlinux/base
FROM $baseimage

LABEL maintainers="Lukas Nellen <lukas@nucleares.unam.mx>" \
      name="Software install environment" 

RUN pacman --noconfirm --noprogressbar -Syu \
# build tools and helpers
    binutils \
    doxygen \
    gcc \
    gcc-fortran \
    git \
    less \
    make \
    awk \
    patch \
    python2 \
    python \
    rsync \
    subversion \
    which \
    file \
# package headers
    bzip2 \
    libpng \
#    libjpeg-dev \
    libmariadbclient \
    libx11 \
    libxpm \
    libxft \
    libxext \
#    python-dev \
    zlib \
# for running final software
    wget

#\
#  && \
# cleanup
#    apt-get clean && rm -rf /var/lib/apt/lists/*

