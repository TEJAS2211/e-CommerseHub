FROM node:18-alpine

WORKDIR /app

# Install dependencies first (cache friendly)
COPY package*.json ./
RUN npm ci --only=production

# Copy source
COPY . .

EXPOSE 3001

CMD ["npm", "run", "start"]
