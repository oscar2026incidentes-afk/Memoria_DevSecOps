FROM ubuntu:22.04

# Evitar preguntas interactivas (tzdata, etc.)
ENV DEBIAN_FRONTEND=noninteractive

# Actualizar repos e instalar Apache, PHP, Git y tzdata sin interacción
RUN apt-get update && \
    apt-get install -y apache2 php libapache2-mod-php git tzdata && \
    rm -rf /var/lib/apt/lists/*

# Descargar tu repositorio y copiar la carpeta app
RUN git clone https://github.com/oscar2026incidentes-afk/Memoria_DevSecOps /tmp/repo && \
    cp -r /tmp/repo/tareaDockerPHP/app /tmp/app

# Copiar la aplicación al directorio web de Apache
RUN rm -rf /var/www/html/* && \
    cp -r /tmp/app/* /var/www/html/

# Exponer el puerto 80
EXPOSE 80

# Iniciar Apache en primer plano
CMD ["apachectl", "-D", "FOREGROUND"]
