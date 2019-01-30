BootStrap: docker
FROM: ubuntu:16.04

%help
    This container runs Cylc 7.8.1.

%labels
    Maintainer Bruno P. Kinoshita
    Version 0.1
    Cylc_Version 7.8.1
    Python_Version 2.7.12

%post
    apt-get update && apt-get --no-install-recommends -y install \
        at \
        build-essential \
        git \
        graphviz libgraphviz-dev \
        pkg-config \
        python-gtk2-dev \
        python-pip \
        python-wheel \
        python-pygraphviz \
        python python-dev python-pip \
        python-setuptools \
        less \
        sqlite \
        time \
        texlive-latex-base \
    && pip install \
        pycodestyle \
        pyopenssl

    git clone --branch 7.8.1 https://github.com/cylc/cylc.git /opt/cylc/

    cp /opt/cylc/usr/bin/cylc /usr/local/bin/cylc

%runscript
    exec /usr/local/bin/cylc "$@"
