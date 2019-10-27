# Base Image
FROM node:alpine

WORKDIR '/app'

# Install deps
COPY package.json .
RUN npm install
COPY . .

# Startup command
CMD [ "npm", "start" ]