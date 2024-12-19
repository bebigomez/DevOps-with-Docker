FROM node:16

# Exponer el puerto 5001
EXPOSE 5001

# Definir el directorio de trabajo
WORKDIR /usr/src/app

# Copiar los archivos al contenedor
COPY . .

# Instalar las dependencias
RUN npm install

# Construir el proyecto pasándole la url a la cual se realizarán las solicitudes al backend
RUN REACT_APP_BACKEND_URL=http://localhost:8080/ npm run build

# Instalar 'serve' globalmente
RUN npm install -g serve

# Usar 'serve' para servir el contenido en el puerto 5001
CMD ["serve", "-s", "build", "-l", "5001"]
