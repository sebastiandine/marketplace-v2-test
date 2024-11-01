FROM node:20.13-bullseye

# enable React Hot Reload in Container
ENV WATCHPACK_POLLING=true

# install dependencies from package manager
RUN apt update && apt install -y \
    sudo \
    git \
    curl wget

# create 'dev' user, add it to sudo group and set password
RUN mkdir /home/dev
RUN useradd dev && chown -R dev /home/dev
RUN adduser dev sudo
RUN echo "dev:dev"|chpasswd 