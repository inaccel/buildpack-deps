FROM ruby AS fpm
LABEL maintainer=InAccel

RUN apt-get update \
 && apt-get install --yes \
		rpm \
 && rm --force --recursive /var/lib/apt/lists/*

ARG BACKPORTS_VERSION=3.16.0
ARG FPM_VERSION=1.11.0
RUN gem install \
		backports:${BACKPORTS_VERSION} \
		fpm:${FPM_VERSION}
