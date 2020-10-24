FROM ubuntu
#FROM ubuntu:18.04

LABEL maintainer="adam@groundupdb.com"

# Configure tzdata so image build does not hang
ENV TZ=Europe/London
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# base packages
RUN apt-get update && \
  apt-get install -yy build-essential cmake make && \
  cmake --version
RUN apt-get clean
