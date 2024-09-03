# Se usara una imagen de Node.js oficial en su version 14
FROM node:14

# Se establece el directorio de trabajo del contenedor contenedor
# para guardar los futuros archivos
WORKDIR /usr/src/app

# Copiar el archivo package.json y package-lock.json en /usr/src/app
COPY package*.json ./

# Se ejecuta en comando install de npm para descargar las dependencias necesarias para
# el correcto funcionamiento del aplicativo
RUN npm install

# Copia el resto de la aplicación al contenedor
COPY . .

# Expone el puerto que la aplicación usará
EXPOSE 3001

# Define el comando para ejecutar la aplicación "node index.js"
CMD ["node", "index.js"]