# Use lightweight Node.js image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Production environment
ENV NODE_ENV=production

# Copy package files
COPY package*.json ./

# Install production dependencies
RUN npm install --omit=dev

# Copy backend source code
COPY src ./src

# Expose backend port
EXPOSE 3000

# Start backend
CMD ["node", "src/server.js"]
