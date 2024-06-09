FROM node:18-alpine AS builder

# Set the working directory in the container.
WORKDIR /app

# Copy package.json and package-lock.json to the working directory.
COPY package*.json ./

# Install dependencies.
RUN npm install

# Copy the rest of the application code to the working directory.
COPY . .

# List the files and folders in the working directory
# RUN ls -la /app

# Build the Next.js application.
RUN npm run build

# Expose port 3000 to the outside world.
EXPOSE 3000

# Start the Next.js application.
CMD ["npm", "start"]
