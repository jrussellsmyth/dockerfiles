# Run httpyac in a container:
#
# docker run --rm -it \
#	-v $PWD:/usr/src \
#	jrussellsmyth/httpyac \
#   file.http -a
#
# Helpful Hint. Installing node dependencies such as jsonpath without installing node
# docker run --rm -it --workdir=/usr/src/app -v $PWD:/usr/src/app node:alpine npm install jsonpath
FROM node:alpine
LABEL maintainer "Russell Smyth <jrussell.smyth@gmail.com>"

RUN npm install --global httpyac

WORKDIR /usr/src

ENTRYPOINT [ "httpyac" ]