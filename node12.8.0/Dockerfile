FROM debian:10
RUN apt update && apt upgrade -y && apt install curl mariadb-client -y
RUN curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash

WORKDIR /code

COPY .nvmrc /code/.nvmrc
RUN /bin/bash -l -c "nvm install;" \
    "nvm use;"

RUN apt-get clean
RUN apt-get autoclean