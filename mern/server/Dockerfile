# Use the official Node.js image as the base image
FROM node:18



# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

ENV MONGODB_URI="mongodb://localhost:27017"

# Expose a port (if your Node.js app listens on a specific port)
EXPOSE 5050

# Command to start your Node.js app
CMD ["node", "server.mjs"]
