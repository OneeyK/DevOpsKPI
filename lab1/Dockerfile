
FROM buildpack-deps:bullseye
# Install node inside the container
RUN curl --silent --location https://deb.nodesource.com/setup_19.x | bash -
RUN apt-get install -y \
  nodejs
# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package*.json ./

RUN npm install

# Bundle app source
COPY . .

EXPOSE 80
CMD [ "node", "server.js" ]
