# Use Node.js 20.17.0 base image
FROM node:20.17.0

# Set working directory
WORKDIR /src

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm cache clean --force
RUN npm install --legacy-peer-deps

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on, here, I was using port 3001
EXPOSE 3001

# Command to run the app
CMD [  "npm", "run", "start:dev"]