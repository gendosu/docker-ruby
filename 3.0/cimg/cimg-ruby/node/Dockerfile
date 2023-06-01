ARG RUBY_VERSION 3.0.5

FROM cimg/ruby:$RUBY_VERSION-node

RUN sudo apt-get update -qq && \
	  sudo apt-get upgrade -y; \
    DEBIAN_FRONTEND=noninteractive sudo apt-get install -yq --no-install-recommends \
      default-mysql-client \
      build-essential \
      vim \
      git \
      curl \
      less \
      xvfb \
      ffmpeg \
      poppler-utils \
      graphviz \
      qtbase5-dev \
      libqt5webkit5-dev \
      gstreamer1.0-plugins-base \
      gstreamer1.0-tools \
      gstreamer1.0-x \
      libprotobuf-dev \
      libprotoc-dev \
      protobuf-compiler \
      bison \
      dpkg-dev \
      libgdbm-dev \
      pkg-config \
      libxml2-dev \
      libcurl4-openssl-dev \
      imagemagick \
      ;
