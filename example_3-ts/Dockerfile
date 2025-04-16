# Базовый образ Node.js
FROM node:16

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем package.json и package-lock.json в контейнер
COPY package*.json /app/

# Устанавливаем зависимости
RUN npm install

# Копируем весь проект в контейнер
COPY . /app/

# Компилируем TypeScript в JavaScript
RUN npm run build

# Экспонируем порт, на котором будет работать сервер
EXPOSE 8080

# Запускаем сервер, указываем путь к скомпилированному файлу
CMD ["node", "dist/server.js"]
