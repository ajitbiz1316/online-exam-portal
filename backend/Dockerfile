# Use the official Node.js image as a base
FROM node:16 AS build

ENV NODE_ENV=docker

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install the project dependencies
RUN npm ci

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 5000


# Command to run the application
CMD ["npm", "start"]

