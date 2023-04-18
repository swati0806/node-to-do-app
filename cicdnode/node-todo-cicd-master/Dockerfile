FROM node:12.2.0-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Run tests
RUN npm run test

# Expose the application port
EXPOSE 8000

# Start the application
CMD ["node", "app.js"]
