# Use the official Node.js image as a base
FROM node:16 AS build

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install the project dependencies
RUN npm ci

# Copy the rest of the application code
COPY . .

# Build the application (modify this command based on your build process)
RUN npm run build

# Expose the port the app runs on
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]

