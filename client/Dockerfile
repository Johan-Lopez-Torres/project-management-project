# Usa una imagen base de Node.js
FROM node:18-alpine AS base

# Configura el directorio de trabajo
WORKDIR /app

# Copia los archivos package.json y package-lock.json
COPY package*.json ./

# Instala las dependencias de producción
RUN npm install --production

# Copia el resto del código de la aplicación
COPY . .

# Construye la aplicación Next.js
RUN npm run build

# Expone el puerto donde correrá la app
EXPOSE 3000

# Comando para ejecutar la aplicación
CMD ["npm", "start"]
