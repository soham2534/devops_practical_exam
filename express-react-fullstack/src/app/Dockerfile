# Dockerfile for React app
FROM node:14 as build

WORKDIR /app

COPY app/package*.json ./app/

RUN npm install --prefix ./app

COPY app/ ./app

RUN npm run build --prefix ./app

FROM nginx:alpine
COPY --from=build /app/app/build /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
