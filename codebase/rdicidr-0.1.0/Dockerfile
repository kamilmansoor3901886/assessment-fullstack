# Use an official Node.js runtime as base
FROM node:15-alpine

# Set working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first (for caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy rest of the application
COPY . .

# Build the app (optional if your app has build step)
RUN npm run build

# Expose port 8080
EXPOSE 8080

# Start the app
CMD ["npm", "start"]
