FROM centos:7
LABEL maintainer="simon@mccartney.ie"

RUN yum install -y \
  python-setuptools \
	ruby-devel \
	git \
	gcc \
	make \
	ruby \
	rpm-build \
	rpm-sign && yum clean all

RUN easy_install pip && pip install --upgrade setuptools
RUN gem install fpm --no-ri --no-rdoc

VOLUME [ "/tmp/fpm" ]
WORKDIR /tmp/fpm

ENTRYPOINT [ "/usr/local/bin/fpm" ]
CMD [ "--help" ]
