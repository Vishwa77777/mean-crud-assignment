# Build Angular app
FROM node:18-alpine AS build

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

# Default Angular production build
RUN npm run build --prod

# Serve built files with Nginx
FROM nginx:alpine

# Copy whatever is in dist/ to nginx html folder
COPY --from=build /app/dist/ /usr/share/nginx/html

EXPOSE 80
