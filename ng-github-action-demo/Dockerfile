# Use official Node.js LTS Alpine image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Install Angular CLI globally
RUN npm install -g @angular/cli

# Copy dependency files first (to leverage caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# Expose Angular's default dev server port
EXPOSE 4200

# Serve the Angular application
CMD ["npm", "run", "docker-run"]
