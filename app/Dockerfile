# Use an official Node.js runtime as a parent image
FROM node:18-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
# This allows Docker to cache the npm install step if only source code changes
COPY package*.json ./

# Install application dependencies
RUN npm install

# Copy the rest of the application source code to the working directory
COPY . .

# Expose the port your application listens on
EXPOSE 3000

# Define the command to run the application when the container starts
CMD ["node", "src/index.ts"]