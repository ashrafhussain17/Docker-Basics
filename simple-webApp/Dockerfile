# Specify a base image

FROM node:alpine

# Set up working directory
WORKDIR /usr/app

# copying package.json to the temporary container
# only package.json is copying because of caching
COPY ./package.json ./

# Install some dependencies
RUN npm install

# Now copy everything except package,json
COPY ./ ./

# Default command
CMD ["npm", "start"]