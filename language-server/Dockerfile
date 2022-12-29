/FROM debian
RUN apt update && apt upgrade -y && apt install curl -y
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash - && apt-get install -y nodejs
RUN npm install -g typescript-language-server
