# Run httpyac in a container:
#
# docker run --rm -it \
#	-v $PWD:/workspace \
#	jrussellsmyth/httpyac
#
FROM node:alpine
LABEL maintainer "Russell Smyth <jrussell.smyth@gmail.com>"

RUN apk --no-cache add \
	file \
	libpng

RUN set -x \
	&& apk add --no-cache --virtual .build-deps \
		autoconf \
		automake \
		build-base \
		libpng-dev \
		nasm \
	&& npm install --global httpyac \
	&& apk del .build-deps

RUN mkdir /workspace

WORKDIR /workspace

ENTRYPOINT [ "httpyac" ]