# Build the app
FROM node:alpine as build-phase
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# Run phase
# expose port for elastic beanstalk 
FROM nginx
EXPOSE 80
COPY --from=build-phase /app/build /usr/share/nginx/html


