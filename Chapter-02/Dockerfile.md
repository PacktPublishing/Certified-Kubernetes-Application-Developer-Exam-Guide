# Pull latest node.js image file, here you can define the version of your choice for example 16
FROM node:latest

# Create and set working directory for the application inside container
WORKDIR /usr/src/app

# Install app dependencies
# COPY source code application source to working directory
COPY . ./

RUN npm install

# If we want to build our code development environment 
# RUN npm ci --only=dev

# Start the nodejs server on port 8080
EXPOSE 8080
CMD ["node", "server.js"]
