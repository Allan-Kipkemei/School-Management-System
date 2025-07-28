FROM node:18-alpine

# Create app directory
WORKDIR /app

# Copy and install dependencies
COPY package.json yarn.lock ./
RUN yarn install

# Copy rest of the backend files
COPY . .

# Expose port and start app
EXPOSE 5000
CMD ["node", "index.js"]
