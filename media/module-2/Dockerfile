# Use the official Node.js image, version 6.x alpine branch
FROM node:6-alpine

# Install tini using alpine package manager
RUN apk add --no-cache tini

# Set working directory to /usr/src/app
WORKDIR /usr/src/app

# Copy the package.json file and install dependencies
COPY package.json ./
RUN npm install && npm cache clean --force

# Copy the rest of the application files
COPY . .

# Expose port 80 to map to the app's port 3000
EXPOSE 80

# Run the app using tini and redirect host port 80 to container port 3000
CMD ["/sbin/tini", "--", "node", "./bin/www"]