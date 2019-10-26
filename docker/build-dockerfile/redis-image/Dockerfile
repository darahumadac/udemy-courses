# Use existing docker image as base
FROM alpine

# Download and install dependencies
RUN apk add --update redis
RUN apk add --update gcc

# Startup command for container
CMD ["redis-server"]