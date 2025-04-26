# Backend Dockerfile
FROM node:18

# Working directory
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the backend code
COPY . .

# Expose backend server port
EXPOSE 5000

# Start the backend server
CMD ["npm", "run", "dev"]
