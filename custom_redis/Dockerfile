# Specify a base image
FROM alpine
# Create a work directory
WORKDIR /user/app
# Download and install Redis
RUN apk add --update redis
# Set a default command for container
CMD [ "redis-server" ]