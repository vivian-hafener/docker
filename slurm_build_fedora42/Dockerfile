FROM fedora:42
RUN dnf install -y @development-tools
RUN dnf install -y https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
RUN dnf -y install \
	    clang \
	    clang-analyzer \
	    expect \
	    gtk2-devel \
	    hdf5-devel \
	    http-parser-devel \
	    hwloc-devel \
	    json-c-devel \
	    libcurl-devel \
	    libjwt-devel \
	    libevent-devel \
	    libibmad-devel \
	    libibumad-devel \
	    OpenIPMI \
	    libssh2-devel \
	    libyaml-devel \
	    lua-devel \
	    lz4-devel \
	    man \
	    man2html \
	    mariadb \
	    mariadb-devel \
	    munge \
	    munge-devel \
	    ncurses-devel \
	    numactl-devel \
	    openssl-devel \
	    pam-devel \
	    perl-ExtUtils-MakeMaker \
	    perl-ExtUtils-ParseXS \
	    pmix-devel \
	    python3 \
	    readline-devel \
	    rrdtool-devel \
	    vim \
	    which
RUN echo "thisismysecretmungekeythatis32bytes" > /etc/munge/munge.key
RUN chown munge:munge /etc/munge/munge.key
RUN chmod 0400 /etc/munge/munge.key
WORKDIR /slurm
CMD ["/bin/bash"]
