# Базовий образ Node
FROM node:18

# Робоча директорія
WORKDIR /app/server

# Копіюємо package.json та package-lock.json
COPY server/package*.json ./

# Копіюємо Prisma, щоб postinstall міг знайти schema.prisma
COPY server/prisma ./prisma

# Встановлюємо залежності (включно з postinstall)
RUN npm install

# Копіюємо весь інший код сервера
COPY server/ ./

# Виставляємо порт
EXPOSE 5000

# Запуск сервера
CMD ["npm", "start"]



