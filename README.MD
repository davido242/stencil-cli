STEPS TO DOCKERIZING STENCIL-CLI

*CREATE THEME FOLDER
*CREATE A DOCKERFILE WITH THE FOLLOWING:
# use official node parent image
FROM node:10
# set container working directory
WORKDIR /theme
# install the cli
RUN npm -g config set user root
RUN npm install -g @bigcommerce/stencil-cli
# publish cli default port
EXPOSE 3000

*OPEN TERMINAL AND RUN: 'docker build -t docker-stencil https://github.com/aglensmith/docker-stencil-cli.git'
*NEXT>>RUN: 'docker run -it -v /$(PWD) -p3000:3000 docker-stencil //bin/bash'
* ENTER "exit" command
*Clone the Official Repo: "git clone https://github.com/bigcommerce/cornerstone.git"
*Re-run: "docker run -it -v /$(PWD) -p3000:3000 docker-stencil //bin/bash"
*Run: "stencil init"
* Request for store URL, API and Token to continue....
* ENTER "exit" command to halt



TO INITIALIZE SUBSEQUENTLY:
*RUN: "docker run -it -v /$(PWD) -3000:3000 docker-stencil //bin/bash"
*RUN: "stencil init"