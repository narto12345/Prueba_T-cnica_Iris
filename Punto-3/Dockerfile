# Usa una imagen base oficial de Node.js
FROM node:14

# Establece el directorio de trabajo en el contenedor
WORKDIR /usr/src/app

# Copia el archivo package.json y package-lock.json (si existe)
COPY package*.json ./

# Instala las dependencias
RUN npm install

# Copia el resto de la aplicación al contenedor
COPY . .

# Expone el puerto que la aplicación usará
EXPOSE 3000

# Define el comando para ejecutar la aplicación
CMD ["node", "index.js"]