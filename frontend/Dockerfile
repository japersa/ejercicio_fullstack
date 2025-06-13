FROM node:22.14.0-slim

# Configurar el directorio de trabajo
WORKDIR /app

# Copiar archivos de mi proyecto
COPY . .

# Instalar dependencias
RUN npm install

ARG VITE_BACKEND_URL
ENV VITE_BACKEND_URL=${VITE_BACKEND_URL}

RUN echo "VITE_BACKEND_URL is set to $VITE_BACKEND_URL"

# Construir la aplicación
RUN npm run build

EXPOSE 5136

# Comando para iniciar la aplicación
CMD ["npm", "start"]