FROM node:18

WORKDIR /app

COPY server/package*.json ./server/
RUN cd server && npm install

COPY server ./server
COPY prisma ./prisma

WORKDIR /app/server

RUN npx prisma generate --schema=../prisma/schema.prisma

EXPOSE 5000
CMD ["npm", "start"]
