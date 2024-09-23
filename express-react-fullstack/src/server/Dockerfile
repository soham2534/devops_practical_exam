# Dockerfile for Node.js server
FROM node:14

WORKDIR /app

COPY server/package*.json ./server/

RUN npm install --prefix ./server

COPY server/ ./server

EXPOSE 5000
CMD ["npm", "start", "--prefix", "server"]
