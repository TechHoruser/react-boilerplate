# pull official base image
FROM node:18.10-alpine3.15

# set working directory
WORKDIR /app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# install app dependencies
COPY package*.json ./
RUN npm install --silent
RUN npm install react-scripts -g --silent

# add app
COPY . ./

# start app
# CMD ["tail", "-f", "/dev/null"]
CMD ["npm", "start"]
