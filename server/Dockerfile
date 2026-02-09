FROM node:18

WORKDIR /app/server

COPY server/package*.json ./
RUN npm install

COPY server ./ 

RUN npx prisma generate

EXPOSE 5000
CMD ["npm", "start"]
