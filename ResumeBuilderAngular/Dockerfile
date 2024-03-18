FROM node:18 AS build
WORKDIR /app
COPY . .
RUN npm install --force
RUN npm run build

# --- Release with Alpine ----
FROM nginx:alpine
COPY --from=build /app/dist/resumebuilder /usr/share/nginx/html
EXPOSE 80
CMD [ "nginx","-g","daemon off;" ]