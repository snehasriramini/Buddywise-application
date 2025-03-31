# Use Node.js image
FROM node:18

# Set working directory inside the container
WORKDIR /app

# Copy package.json first
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy everything else
COPY . .

# Expose the port React runs on
EXPOSE 3000

# Start the React app
CMD ["npm", "start"]
