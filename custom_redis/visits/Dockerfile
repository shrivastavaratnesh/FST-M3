#Base image
FROM node:16-alpine
#Work directory
WORKDIR /user/app
#Copy file to work directory
COPY ./package.json .
#install dependency
RUN npm install
COPY . .
#Start application
CMD ["npm","start"]