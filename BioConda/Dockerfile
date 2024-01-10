# use latest ubuntu as the base image
FROM ubuntu:latest

# set env vars
# ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

# install packages
RUN apt-get update && \
    apt-get install -y wget bzip2 && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# install miniconda
RUN wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O /tmp/miniconda.sh && \
    bash /tmp/miniconda.sh -b -p /opt/conda && \
    rm /tmp/miniconda.sh

# add conda to the PATH
ENV PATH=/opt/conda/bin:$PATH

# install Bioconda
RUN conda config --add channels defaults && \
    conda config --add channels bioconda && \
    conda config --add channels conda-forge

# install any bioconda packages needed
# example: samtools
RUN conda install -y samtools

# start an interactive shell when the container runs
CMD ["/bin/bash"]
