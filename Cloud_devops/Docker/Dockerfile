# Usa la imagen base de Debian
FROM debian:latest

# Actualiza el sistema e instala Apache
RUN apt-get update && apt-get install -y apache2 && apt-get clean && rm -rf /var/lib/apt/lists/*

# Copia el archivo index.html al directorio de documentos de Apache
ADD index.html /var/www/html/

# Expone el puerto 80 para que se pueda acceder al servidor web
EXPOSE 80

# Define el comando de entrada para iniciar Apache en primer plano
ENTRYPOINT ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
