# Базовий образ Node
FROM node:18

# Робоча директорія
WORKDIR /app/server

# Копіюємо package.json та package-lock.json для швидшої установки залежностей
COPY server/package*.json ./

# Встановлюємо залежності
RUN npm install

# Копіюємо весь код сервера (включно з Prisma)
COPY server/ ./

# Виставляємо порт
EXPOSE 5000

# Запуск сервера
CMD ["npm", "start"]


