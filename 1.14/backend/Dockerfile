# Usar la imagen oficial de Golang versión 1.16 como base
FROM golang:1.16

# Exponer el puerto 8080 para que pueda ser accesible desde fuera del contenedor
EXPOSE 8080

# Establecer el directorio de trabajo dentro del contenedor
WORKDIR /usr/src/app

# Copiar todo el contenido del directorio actual al contenedor
COPY . .

# Definir una variable de entorno llamada PORT, que se usará para configurar el puerto de la aplicación
ENV PORT=8080

# Definir una variable de entorno llamada REQUEST_ORIGIN, que se usará para especificar el origen desde el cual se permiten solicitudes (CORS)
ENV REQUEST_ORIGIN="http://localhost:5001"

# Ejecutar el comando `go build` para construir el binario llamado "server" a partir del código fuente de Go
RUN go build

# Comando por defecto para ejecutar el binario "server" cuando el contenedor se inicie
CMD ["./server"]
