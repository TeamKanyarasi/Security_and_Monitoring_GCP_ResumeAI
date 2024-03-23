FROM node:18 AS build
WORKDIR /app
COPY . .
RUN npm install --force
RUN npm install -g typescript
ENV JWT_SECRET_KEY="your-jwt-secret-key"
ENV MONGO_URL="your-mongo-url"
ENV OPENAI_KEY="your-api-key"
ENV GMAIL_USER="your-gmail"
ENV GMAIL_PASS="your-gmail-pass"
ENV FRONT_END="your-frontend-url"
RUN tsc --project tsconfig.json 

# --- Release with Alpine ----
FROM node:18-alpine
COPY --from=build /app ./
EXPOSE 4292
CMD [ "npm", "start" ]