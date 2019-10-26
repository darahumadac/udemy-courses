# Base image <repo_name:version>
# alpine version is a term referring to a stripped down version of the image
FROM node:alpine

# Change working directory. all following commands will be executed relative to this path
WORKDIR /usr/app

# Install deps / copy files needed to run the app
# this takes the base image and creates a temporary container and executes the command 
# in the container
# at this point, the only available files and folders inside temporary container are 
# whatever is there in the base image
COPY ./package.json ./
RUN npm install
# Split copying of files to avoid invalidating build cache (unnecessary rebuild) 
# and re-downloading of dependencies when updating index.json
COPY ./ ./

# Startup command
CMD ["npm", "start"]
