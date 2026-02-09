FROM node:18

# Робоча папка для всього додатку
WORKDIR /app

# Копіюємо тільки package.json і package-lock.json
COPY server/package*.json ./server/

WORKDIR /app/server

# Встановлюємо залежності
RUN npm install

# Копіюємо все з server (включно з prisma)
COPY server/ ./ 

EXPOSE 5000

CMD ["npm", "start"]

