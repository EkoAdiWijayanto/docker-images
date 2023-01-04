FROM debian
RUN apt-get update && apt-get upgrade -y && apt-get install curl mariadb-client git jq -y 
RUN curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash

WORKDIR /code

COPY .nvmrc /code/.nvmrc
RUN /bin/bash -l -c "nvm install;" \
    "nvm use;"
    
RUN /bin/bash -l -c "npm install -g --unsafe-perm cross-env babel-cli"

RUN apt-get clean
RUN apt-get autoclean
