# Frontend Dockerfile
FROM node:18

# Working directory
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the frontend code
COPY . .

# Build frontend project (Vite build)
RUN npm run build

# Install serve to host production build
RUN npm install -g serve

# Expose frontend port
EXPOSE 3000

# Serve frontend build
CMD ["serve", "-s", "dist"]
