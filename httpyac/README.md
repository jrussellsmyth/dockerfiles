# httpyac
A docker image to run [httpYac](https://httpyac.github.io/)

## Use
`docker run --rm -it -w $PWD -v $PWD:$PWD jrussellsmyth/httpyac test.http -a`

Alternately, you can mount your local dir to /usr/src, the default WORKDIR in the image.

Module dependencies must be installed in the working directory. 

## Installing node dependencies in your project without installing node
To install node modules in your project without installing node (vscode and standalone bring their own node with them)

`docker run --rm -it --workdir=/usr/src/app -v $PWD:/usr/src/app node:alpine npm install jsonpath`

## Try It
In this folder run

`docker run --rm -it --workdir=/usr/src/app -v $PWD:/usr/src/app node:alpine npm install jsonpath`

`docker run --rm -it -w $PWD -v $PWD:$PWD  jrussellsmyth/httpyac test.http -a`
