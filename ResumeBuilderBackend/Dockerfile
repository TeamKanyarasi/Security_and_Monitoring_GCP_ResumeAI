FROM node:18 AS build
WORKDIR /app
COPY . .
RUN npm install --force
RUN npm install -g typescript
ENV JWT_SECRET_KEY="56dcb5a099152e64d38146a3d727c4d2e90307e6a8df3a94f3c1095725b68840"
ENV MONGO_URL="mongodb+srv://charanyandrapu09:Charan6055@clusterblacksquad.vdh7yzc.mongodb.net/resume_builder"
ENV OPENAI_KEY="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"
ENV GMAIL_USER="charanyandrapu09@gmail.com"
ENV GMAIL_PASS="Charan@6055"
ENV FRONT_END="http://eager_mclean:80/"
RUN tsc --project tsconfig.json 

# --- Release with Alpine ----
FROM node:18-alpine
COPY --from=build /app ./
EXPOSE 4292
CMD [ "npm", "start" ]