# Minimal python container
# based on [progrium/busybox](https://github.com/progrium/busybox) and [Anaconda Python Distribution](https://store.continuum.io/cshop/anaconda/)

FROM gliderlabs/alpine:latest
MAINTAINER Nick Roth
RUN apk-install bash bzip2 zlib
RUN wget http://repo.continuum.io/miniconda/Miniconda-latest-Linux-x86_64.sh -O /miniconda.sh \
 && /bin/bash miniconda.sh -p /miniconda -b \
 && rm /miniconda.sh
ENV PATH=/miniconda/bin:${PATH}
RUN conda update -y conda
