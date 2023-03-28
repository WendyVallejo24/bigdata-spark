# os base
FROM debian:bullseye

# run apt-get
RUN apt-get update

# install some utilities
RUN apt-get install -y curl make g++

# Install Node.js and npm.
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get install -y nodejs

# add package.json
ADD package.json /package.json
RUN npm install

WORKDIR /src

EXPOSE 8080

CMD ["node", "/src/server.js"]
