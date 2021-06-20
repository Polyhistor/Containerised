# Phase 1 - build stage
FROM node:alpine AS build
WORKDIR /app
COPY . .
RUN  npm ci && npm run build

# Phase 2 - 
FROM nginx:1.17-alpine
COPY --from=build app/build /usr/share/nginx/html


